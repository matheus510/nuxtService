<template>
<table cellspacing="0" cellpadding="0" width="100%">
    <tr>
        <td class="template-header">
            <table cellpadding="0" cellspacing="0" width="100%">
                <tr>
                    <td class="header-img">
                        <img v-if="this.template.dados.Template.Opcoes['Template Boxnet']"
                             src="`${template.config.urlPage()}/BookContents/Clientes/{{template.dados.Template.IdProdutoMvc}}/img/header.png${template.config.versao}"
                             alt=""/>
                        <img v-if="template.dados.Template.Opcoes['Template Boxnet']"
                             src="{{template.config.urlPage()}}/BookContents/Clientes/0/img/header.png{{template.config.versao}}"
                             alt=""/>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
    <tr>
        <td class="template-botoes">
            <table cellpadding="0" cellspacing="0" width="100%">
                <tr>
                    <td class="data-book">
                        <div>
                            {{ this.template.dados.DataCadastro }}
                        </div>
                    </td>
                    <td width="100" class="botoes">
                        <a v-if="template.navegadoresAntigos"
                           href="{{template.config.urlPage()}}/Visualizar/?b={{template.config.idBookVersao}}&p={{template.dados.IdProduto}}&pmvc={{template.dados.Template.IdProdutoMvc}}">
                            ver todas
                        </a>
                        <a v-if="!template.navegadoresAntigos"
                           href="{{template.config.urlVis()}}/?idBook={{template.config.idBook}}&idProdutoMvc={{template.dados.Template.IdProdutoMvc}}&idNoticia=0">
                            ver todas
                        </a>
                    </td>
                    <td width="100" class="botoes">
                        <a href="{{template.dados.UrlGerarPdf}}">
                            gerar pdf
                        </a>
                    </td>
                </tr>
            </table>
        </td>
    </tr>
</table>
</template>
<script>
export default {
    data: function () {
        return {
            counter: 0
        }
    }
}
</script>
