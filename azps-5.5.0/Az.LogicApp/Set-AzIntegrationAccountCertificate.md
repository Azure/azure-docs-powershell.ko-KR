---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 5b8da61caf8e3a89572f2054aea101a1ad8b70c6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180348"
---
# <span data-ttu-id="e8557-101">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e8557-101">Set-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="e8557-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8557-102">SYNOPSIS</span></span>
<span data-ttu-id="e8557-103">통합 계정 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-103">Modifies an integration account certificate.</span></span>

## <span data-ttu-id="e8557-104">구문</span><span class="sxs-lookup"><span data-stu-id="e8557-104">SYNTAX</span></span>

```
Set-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e8557-105">설명</span><span class="sxs-lookup"><span data-stu-id="e8557-105">DESCRIPTION</span></span>
<span data-ttu-id="e8557-106">**Set-AzIntegrationAccountCertificate** cmdlet은 통합 계정 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-106">The **Set-AzIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="e8557-107">이 cmdlet은 통합 계정 인증서를 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="e8557-108">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-108">Specifying the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="e8557-109">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="e8557-110">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="e8557-111">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="e8557-112">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="e8557-113">예제</span><span class="sxs-lookup"><span data-stu-id="e8557-113">EXAMPLES</span></span>

### <span data-ttu-id="e8557-114">예제 1: 통합 계정 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="e8557-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SubscriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="e8557-115">이 명령은 지정된 리소스 그룹의 통합 계정 인증서를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="e8557-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e8557-116">PARAMETERS</span></span>

### <span data-ttu-id="e8557-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="e8557-117">-CertificateName</span></span>
<span data-ttu-id="e8557-118">통합 계정 인증서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-118">Specifies the name of an integration account certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8557-119">-DefaultProfile</span></span>
<span data-ttu-id="e8557-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e8557-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e8557-121">-Force</span><span class="sxs-lookup"><span data-stu-id="e8557-121">-Force</span></span>
<span data-ttu-id="e8557-122">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-123">-KeyName</span><span class="sxs-lookup"><span data-stu-id="e8557-123">-KeyName</span></span>
<span data-ttu-id="e8557-124">키 자격 증명 모음에서 인증서 키의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-124">Specifies the name of a certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-125">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="e8557-125">-KeyVaultId</span></span>
<span data-ttu-id="e8557-126">키 자격 증명 모음 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-126">Specifies a key vault ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-127">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="e8557-127">-KeyVersion</span></span>
<span data-ttu-id="e8557-128">키 자격 증명 모음의 인증서 키 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-128">Specifies the version of the certificate key in the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-129">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e8557-129">-Metadata</span></span>
<span data-ttu-id="e8557-130">인증서에 대한 메타데이터 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-130">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="e8557-131">-Name</span><span class="sxs-lookup"><span data-stu-id="e8557-131">-Name</span></span>
<span data-ttu-id="e8557-132">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-132">Specifies the name of the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IntegrationAccountName, ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-133">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="e8557-133">-PublicCertificateFilePath</span></span>
<span data-ttu-id="e8557-134">공용 인증서(.cer) 파일의 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-134">Specifies the path of a public certificate (.cer) file.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8557-135">-ResourceGroupName</span></span>
<span data-ttu-id="e8557-136">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-136">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8557-137">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e8557-137">-Confirm</span></span>
<span data-ttu-id="e8557-138">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8557-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8557-139">-WhatIf</span></span>
<span data-ttu-id="e8557-140">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e8557-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8557-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8557-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8557-142">CommonParameters</span></span>
<span data-ttu-id="e8557-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e8557-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8557-144">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e8557-144">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8557-145">입력</span><span class="sxs-lookup"><span data-stu-id="e8557-145">INPUTS</span></span>

### <span data-ttu-id="e8557-146">System.String</span><span class="sxs-lookup"><span data-stu-id="e8557-146">System.String</span></span>

## <span data-ttu-id="e8557-147">출력</span><span class="sxs-lookup"><span data-stu-id="e8557-147">OUTPUTS</span></span>

### <span data-ttu-id="e8557-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e8557-148">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="e8557-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e8557-149">NOTES</span></span>

## <span data-ttu-id="e8557-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8557-150">RELATED LINKS</span></span>

[<span data-ttu-id="e8557-151">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e8557-151">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e8557-152">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e8557-152">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="e8557-153">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="e8557-153">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)


