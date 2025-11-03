<template>
  <div class="flex flex-col items-center p-7">
    <div class="flex flex-col items-center mb-5">
      <h2 class="text-6xl m-5">Confirme sua presença</h2>
      <p class="text-[#BEB4A7] m-2 text-xl">
        Não perca a festa mais assustadora do ano! Confirme já sua presença.
      </p>
    </div>

    <Form class="w-[50%] space-y-6 bg-[#131212] p-6 rounded-xl border border-[#585858] flex flex-col items-center" @submit="onSubmit">
      <FormField v-slot="{ componentField }" name="fullname">
        <FormItem  class="w-full">
          <FormLabel class="mb-3">Nome completo *</FormLabel>
          <FormControl>
            <Input
              type="text"
              placeholder="Seu nome completo"
              v-bind="componentField"
              class="bg-[#181616]"
            />
          </FormControl>
          <FormMessage />
        </FormItem>
      </FormField>

      <FormField v-slot="{ componentField }" name="email">
        <FormItem class="w-full">
          <FormLabel class="mb-3">Email *</FormLabel>
          <FormControl>
            <Input
              type="email"
              placeholder="seuemail@exemplo.com"
              v-bind="componentField"
              class="bg-[#181616]"
            />
          </FormControl>
          <FormMessage />
        </FormItem>
      </FormField>

      <FormField v-slot="{ componentField }" name="guests">
        <FormItem class="w-full">
          <FormLabel class="mb-3">Número de convidados</FormLabel>
          <Select v-bind="componentField">
            <FormControl>
              <SelectTrigger class="bg-[#181616]">
                <SelectValue placeholder="Selecione o número de convidados" />
              </SelectTrigger>
            </FormControl>
            <SelectContent>
              <SelectGroup>
                <SelectItem
                  v-for="i in 10"
                  :key="i"
                  :value="i.toString()"
                  class="bg-[#181616] font-bold hover:bg-[#252525]"
                >
                  {{ i }}
                </SelectItem>
              </SelectGroup>
            </SelectContent>
          </Select>
          <FormMessage />
        </FormItem>
      </FormField>

      <FormField v-slot="{ componentField }" name="costume">
        <FormItem class="w-full">
          <FormLabel class="mb-3">Sua Fantasia</FormLabel>
          <FormControl>
            <Input
              type="text"
              placeholder="Drácula, Bruxa, Zumbi..."
              v-bind="componentField"
              class="bg-[#181616]"
            />
          </FormControl>
          <FormMessage />
        </FormItem>
      </FormField>

      <FormField v-slot="{ componentField }" name="message">
        <FormItem class="w-full">
          <FormLabel class="mb-3">Mensagem (Opcional)</FormLabel>
          <FormControl>
            <Textarea
              placeholder="Deixe sua mensagem..."
              v-bind="componentField"
              class="bg-[#181616]"
            />
          </FormControl>
          <FormMessage />
        </FormItem>
      </FormField>

      <Button type="submit" variant="default" class="flex items-center justify-center gap-2 h-10 w-full hover:bg-[#f06e4290] hover:cursor-pointer font-bold">
        <p class="text-xl">🎃</p>
        <p class="text-xl">CONFIRMAR PRESENÇA AGORA!</p>
      </Button>

      <p class="text-[#BEB4A7]">Dúvidas? Entre em contato:</p>
    </Form>
  </div>
</template>

<script setup lang="ts">
import { useForm } from 'vee-validate'
import { toTypedSchema } from '@vee-validate/zod'
import * as z from 'zod'

import { Button } from '@/components/ui/button'
import {
  FormControl,
  FormField,
  FormItem,
  FormLabel,
  FormMessage,
} from '@/components/ui/form'
import { Input } from '@/components/ui/input'
import {
  Select,
  SelectContent,
  SelectGroup,
  SelectItem,
  SelectTrigger,
  SelectValue,
} from '@/components/ui/select'
import { Textarea } from '@/components/ui/textarea'

const formSchema = toTypedSchema(
  z.object({
    fullname: z.string().min(2).max(50),
    email: z.string().email(),
    guests: z.string().min(1),
    costume: z.string().min(2).max(50),
    message: z.string().optional(),
  }),
)

const { handleSubmit } = useForm({
  validationSchema: formSchema,
})

const onSubmit = handleSubmit((values) => {
  console.log('Form submitted!', values)
})
</script>

<style lang="scss" scoped>
h2 {
  font-family: var(--font-title);
  background-image: linear-gradient(355deg, var(--color-primary) 30%, var(--color-secondary) 90%);
  -webkit-background-clip: text;
  background-clip: text;
  -webkit-text-fill-color: transparent;
  color: transparent;
}
</style>
