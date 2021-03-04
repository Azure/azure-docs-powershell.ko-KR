---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 8b1da3fda8c8c016dd9cbe039015553f9073a4b8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008811"
---
# <span data-ttu-id="d9ca5-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9ca5-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="d9ca5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9ca5-102">SYNOPSIS</span></span>
<span data-ttu-id="d9ca5-103">통합 계정 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="d9ca5-104">구문</span><span class="sxs-lookup"><span data-stu-id="d9ca5-104">SYNTAX</span></span>

### <span data-ttu-id="d9ca5-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="d9ca5-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ca5-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="d9ca5-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9ca5-107">둘 다</span><span class="sxs-lookup"><span data-stu-id="d9ca5-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d9ca5-108">설명</span><span class="sxs-lookup"><span data-stu-id="d9ca5-108">DESCRIPTION</span></span>
<span data-ttu-id="d9ca5-109">**New-AzIntegrationAccountCertificate** cmdlet은 통합 계정 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="d9ca5-110">이 cmdlet은 통합 계정 인증서를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="d9ca5-111">통합 계정 이름, 리소스 그룹 이름, 인증서 이름, 키 이름, 키 버전 및 키 자격 증명 모음 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="d9ca5-112">명령줄에서 지정한 템플릿 매개 변수 파일 값은 템플릿 매개 변수 개체의 템플릿 매개 변수 값보다 우선합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="d9ca5-113">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="d9ca5-114">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="d9ca5-115">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="d9ca5-116">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="d9ca5-117">예제</span><span class="sxs-lookup"><span data-stu-id="d9ca5-117">EXAMPLES</span></span>

### <span data-ttu-id="d9ca5-118">예제 1: 통합 계정 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="d9ca5-118">Example 1: Create an integration account certificate</span></span>
```
PS C:\>New-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/<name>
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="d9ca5-119">이 명령은 지정된 리소스 그룹에 통합 계정 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="d9ca5-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d9ca5-120">PARAMETERS</span></span>

### <span data-ttu-id="d9ca5-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="d9ca5-121">-CertificateName</span></span>
<span data-ttu-id="d9ca5-122">통합 계정 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-122">Specifies a name for the integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9ca5-123">-DefaultProfile</span></span>
<span data-ttu-id="d9ca5-124">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="d9ca5-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="d9ca5-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="d9ca5-125">-KeyName</span></span>
<span data-ttu-id="d9ca5-126">키 자격 증명 모음에 인증서 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-126">Specifies the name of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="d9ca5-127">-KeyVaultId</span></span>
<span data-ttu-id="d9ca5-128">키 자격 증명 모음 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-128">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="d9ca5-129">-KeyVersion</span></span>
<span data-ttu-id="d9ca5-130">키 자격 증명 모음에서 인증서 키의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-130">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-131">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="d9ca5-131">-Metadata</span></span>
<span data-ttu-id="d9ca5-132">인증서에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-132">Specifies a metadata object for the certificate.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-133">-Name</span><span class="sxs-lookup"><span data-stu-id="d9ca5-133">-Name</span></span>
<span data-ttu-id="d9ca5-134">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-134">Specifies the name of an integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="d9ca5-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="d9ca5-136">공용 인증서(.cer) 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-136">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: PrivateKey
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: PublicKey, Both
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9ca5-137">-ResourceGroupName</span></span>
<span data-ttu-id="d9ca5-138">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-138">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-139">-확인</span><span class="sxs-lookup"><span data-stu-id="d9ca5-139">-Confirm</span></span>
<span data-ttu-id="d9ca5-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-140">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9ca5-141">-WhatIf</span></span>
<span data-ttu-id="d9ca5-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9ca5-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-143">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9ca5-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9ca5-144">CommonParameters</span></span>
<span data-ttu-id="d9ca5-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9ca5-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="d9ca5-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9ca5-147">입력</span><span class="sxs-lookup"><span data-stu-id="d9ca5-147">INPUTS</span></span>

### <span data-ttu-id="d9ca5-148">System.String</span><span class="sxs-lookup"><span data-stu-id="d9ca5-148">System.String</span></span>

## <span data-ttu-id="d9ca5-149">출력</span><span class="sxs-lookup"><span data-stu-id="d9ca5-149">OUTPUTS</span></span>

### <span data-ttu-id="d9ca5-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9ca5-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="d9ca5-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d9ca5-151">NOTES</span></span>

## <span data-ttu-id="d9ca5-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d9ca5-152">RELATED LINKS</span></span>

[<span data-ttu-id="d9ca5-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9ca5-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="d9ca5-154">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9ca5-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="d9ca5-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="d9ca5-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


