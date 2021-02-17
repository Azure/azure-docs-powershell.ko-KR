---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/import-AzWebAppKeyVaultCertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Import-AzWebAppKeyVaultCertificate.md
ms.openlocfilehash: 61f498a521134ee0abb74f45ff048c94e7c53081
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190505"
---
# <span data-ttu-id="93ffd-101">Import-AzWebAppKeyVaultCertificate</span><span class="sxs-lookup"><span data-stu-id="93ffd-101">Import-AzWebAppKeyVaultCertificate</span></span>

## <span data-ttu-id="93ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="93ffd-103">Key Vault에서 웹앱으로 SSL 인증서를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-103">Import an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="93ffd-104">구문</span><span class="sxs-lookup"><span data-stu-id="93ffd-104">SYNTAX</span></span>

```
Import-AzWebAppKeyVaultCertificate [-KeyVaultName] <String> [-CertName] <String> [-ResourceGroupName] <String>
 [-WebAppName] <String> [-Slot <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="93ffd-105">설명</span><span class="sxs-lookup"><span data-stu-id="93ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="93ffd-106">**Import-AzWebAppKeyVaultCertificate** cmdlet은 SSL 인증서를 Key Vault에서 웹앱으로 가져오습니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-106">The **Import-AzWebAppKeyVaultCertificate** cmdlet imports an SSL certificate to a web app from Key Vault.</span></span>

## <span data-ttu-id="93ffd-107">예제</span><span class="sxs-lookup"><span data-stu-id="93ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="93ffd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="93ffd-108">Example 1</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName "ContosoKeyVault" -CertName "ContosoCertname"
```

<span data-ttu-id="93ffd-109">이 명령은 Key Vault에서 웹앱으로 SSL 인증서를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-109">This command imports an SSL certificate to a web app from Key Vault.</span></span>

### <span data-ttu-id="93ffd-110">예제 2</span><span class="sxs-lookup"><span data-stu-id="93ffd-110">Example 2</span></span>
```powershell
PS C:\> Import-AzWebAppKeyVaultCertificate -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" 
-KeyVaultName  '/subscriptions/[sub id]/resourceGroups/[rg]/providers/Microsoft.KeyVault/vaults/[vault name]' 
-CertName "ContosoCertname"
```

<span data-ttu-id="93ffd-111">이 명령은 리소스 ID를 사용하여 Key Vault에서 웹앱으로 SSL 인증서를 가져올 수 있습니다(일반적으로 Key Vault가 다른 구독에 있는 경우).</span><span class="sxs-lookup"><span data-stu-id="93ffd-111">This command Import an SSL certificate to a web app from Key Vault using resource id (typically if Key Vault is in another subscription).</span></span>

## <span data-ttu-id="93ffd-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93ffd-112">PARAMETERS</span></span>

### <span data-ttu-id="93ffd-113">-CertName</span><span class="sxs-lookup"><span data-stu-id="93ffd-113">-CertName</span></span>
<span data-ttu-id="93ffd-114">keyvault에서 만든 인증서의 KeyVaultCertName</span><span class="sxs-lookup"><span data-stu-id="93ffd-114">KeyVaultCertName of the certificate created in keyvault</span></span>

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

### <span data-ttu-id="93ffd-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93ffd-115">-DefaultProfile</span></span>
<span data-ttu-id="93ffd-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="93ffd-117">-KeyVaultName</span><span class="sxs-lookup"><span data-stu-id="93ffd-117">-KeyVaultName</span></span>
<span data-ttu-id="93ffd-118">keyvault의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-118">The name of the keyvault.</span></span>

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

### <span data-ttu-id="93ffd-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93ffd-119">-ResourceGroupName</span></span>
<span data-ttu-id="93ffd-120">웹앱 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-120">The name of the webapp resource group.</span></span>

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

### <span data-ttu-id="93ffd-121">-Slot</span><span class="sxs-lookup"><span data-stu-id="93ffd-121">-Slot</span></span>
<span data-ttu-id="93ffd-122">웹앱 슬롯의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-122">The name of the webapp slot.</span></span>

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

### <span data-ttu-id="93ffd-123">-WebAppName</span><span class="sxs-lookup"><span data-stu-id="93ffd-123">-WebAppName</span></span>
<span data-ttu-id="93ffd-124">웹앱의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-124">The name of the webapp.</span></span>

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

### <span data-ttu-id="93ffd-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="93ffd-125">-Confirm</span></span>
<span data-ttu-id="93ffd-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="93ffd-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="93ffd-127">-WhatIf</span></span>
<span data-ttu-id="93ffd-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="93ffd-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="93ffd-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="93ffd-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93ffd-130">CommonParameters</span></span>
<span data-ttu-id="93ffd-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="93ffd-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93ffd-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="93ffd-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93ffd-133">입력</span><span class="sxs-lookup"><span data-stu-id="93ffd-133">INPUTS</span></span>

### <span data-ttu-id="93ffd-134">없음</span><span class="sxs-lookup"><span data-stu-id="93ffd-134">None</span></span>

## <span data-ttu-id="93ffd-135">출력</span><span class="sxs-lookup"><span data-stu-id="93ffd-135">OUTPUTS</span></span>

### <span data-ttu-id="93ffd-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span><span class="sxs-lookup"><span data-stu-id="93ffd-136">Microsoft.Azure.Commands.WebApps.Models.WebApp.PSCertificate</span></span>

## <span data-ttu-id="93ffd-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="93ffd-137">NOTES</span></span>

## <span data-ttu-id="93ffd-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="93ffd-138">RELATED LINKS</span></span>
