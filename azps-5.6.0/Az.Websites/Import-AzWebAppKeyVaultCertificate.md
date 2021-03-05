---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: d92aa19573a238d7f54a21f7888bbd93ac07107b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102007419"
---
# <span data-ttu-id="17d92-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="17d92-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="17d92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17d92-102">SYNOPSIS</span></span>
<span data-ttu-id="17d92-103">Key Vault에서 웹앱으로 SSL 인증서를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="17d92-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="17d92-104">구문</span><span class="sxs-lookup"><span data-stu-id="17d92-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="17d92-105">설명</span><span class="sxs-lookup"><span data-stu-id="17d92-105">DESCRIPTION</span></span>
<span data-ttu-id="17d92-106">**Import-AzWebAppKeyVaultCertificate** cmdlet은 Key Vault에서 웹앱으로 SSL 인증서를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="17d92-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="17d92-107">예제</span><span class="sxs-lookup"><span data-stu-id="17d92-107">EXAMPLES</span></span>

### <span data-ttu-id="17d92-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="17d92-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="17d92-109">이 명령은 Key Vault에서 웹앱에 SSL 인증서를 가져온다.</span><span class="sxs-lookup"><span data-stu-id="17d92-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="17d92-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="17d92-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="17d92-111">이 명령은 리소스 ID를 사용하여 Key Vault에서 웹앱으로 SSL 인증서 가져오기(일반적으로 Key Vault가 다른 구독에 있는 경우).</span><span class="sxs-lookup"><span data-stu-id="17d92-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="17d92-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="17d92-112">PARAMETERS</span></span>

### <span data-ttu-id="17d92-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="17d92-113">-CertName</span></span>
<span data-ttu-id="17d92-114">keyvault에서 만든 인증서의 KeyVaultCertName</span><span class="sxs-lookup"><span data-stu-id="17d92-114">KeyVaultCertName of the certificate created in keyvault</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17d92-115">-DefaultProfile</span></span>
<span data-ttu-id="17d92-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="17d92-117">-KeyVaultName</span></span>
<span data-ttu-id="17d92-118">keyvault의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-118">The name of the keyvault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17d92-119">-ResourceGroupName</span></span>
<span data-ttu-id="17d92-120">웹앱 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-120">The name of the webapp resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="17d92-121">-Slot</span></span>
<span data-ttu-id="17d92-122">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-122">The name of the webapp slot.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="17d92-123">-WebAppName</span></span>
<span data-ttu-id="17d92-124">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-124">The name of the webapp.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-125">-확인</span><span class="sxs-lookup"><span data-stu-id="17d92-125">-Confirm</span></span>
<span data-ttu-id="17d92-126">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17d92-127">-WhatIf</span></span>
<span data-ttu-id="17d92-128">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17d92-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17d92-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17d92-130">CommonParameters</span></span>
<span data-ttu-id="17d92-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="17d92-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17d92-132">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="17d92-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17d92-133">입력</span><span class="sxs-lookup"><span data-stu-id="17d92-133">INPUTS</span></span>

### <span data-ttu-id="17d92-134">없음</span><span class="sxs-lookup"><span data-stu-id="17d92-134">None</span></span>

## <span data-ttu-id="17d92-135">출력</span><span class="sxs-lookup"><span data-stu-id="17d92-135">OUTPUTS</span></span>

### <span data-ttu-id="17d92-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="17d92-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="17d92-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="17d92-137">NOTES</span></span>

## <span data-ttu-id="17d92-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="17d92-138">RELATED LINKS</span></span>
