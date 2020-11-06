---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: D9CA9515-5C19-4D63-8D4D-0B288E9309E9
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Set-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: feb885ca6f08a7396fd88db73d48172dc002f055
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534019"
---
# <span data-ttu-id="acd60-101">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="acd60-101">Set-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="acd60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acd60-102">SYNOPSIS</span></span>
<span data-ttu-id="acd60-103">통합 계정 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-103">Modifies an integration account certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="acd60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="acd60-104">SYNTAX</span></span>

```
Set-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="acd60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="acd60-105">DESCRIPTION</span></span>
<span data-ttu-id="acd60-106">**Set-AzureRmIntegrationAccountCertificate** cmdlet은 통합 계정 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-106">The **Set-AzureRmIntegrationAccountCertificate** cmdlet modifies an integration account certificate.</span></span>
<span data-ttu-id="acd60-107">이 cmdlet은 통합 계정 인증서를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-107">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="acd60-108">통합 계정 이름, 리소스 그룹 이름, 인증서 이름 지정</span><span class="sxs-lookup"><span data-stu-id="acd60-108">Specifying the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="acd60-109">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-109">This module supports dynamic parameters.</span></span>
<span data-ttu-id="acd60-110">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-110">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="acd60-111">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-111">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="acd60-112">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-112">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="acd60-113">예제의</span><span class="sxs-lookup"><span data-stu-id="acd60-113">EXAMPLES</span></span>

### <span data-ttu-id="acd60-114">예제 1: 통합 계정 인증서 수정</span><span class="sxs-lookup"><span data-stu-id="acd60-114">Example 1: Modify an integration account certificate</span></span>
```
PS C:\>Set-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegartionAccount31" -CertificateName "IntegrationAccountCertificate01" -KeyName "TestKey" -KeyVersion "1.0" -KeyVaultId "/subscriptions/<subscriptionId>/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/keyvault" -PublicCertificateFilePath "c:\temp\Certificate.cer"
Id                : /subscriptions/<SusbcriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegartionAccount31/certificates/IntegrationAccountCertificate01
Name              : IntegrationAccountCertificate01
Type              : Microsoft.Logic/integrationAccounts/certificates
CreatedTime       : 3/26/2016 6:59:07 PM
ChangedTime       : 3/26/2016 6:59:07 PM
KeyName           : TestKey
KeyVersion        : 1.0
KeyVaultId        : /subscriptions/<SusbcriptionId/resourcegroups/ResourceGroup11/providers/microsoft.keyvault/vaults/testkeyvault
KeyVaultName      : testkeyvault
KeyVaultName      : testkeyvault
PublicCertificate : 
MetaData          :
```

<span data-ttu-id="acd60-115">이 명령은 지정 된 리소스 그룹의 통합 계정 인증서를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-115">This command modifies the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="acd60-116">변수</span><span class="sxs-lookup"><span data-stu-id="acd60-116">PARAMETERS</span></span>

### <span data-ttu-id="acd60-117">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="acd60-117">-CertificateName</span></span>
<span data-ttu-id="acd60-118">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-118">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="acd60-119">-Force</span><span class="sxs-lookup"><span data-stu-id="acd60-119">-Force</span></span>
<span data-ttu-id="acd60-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="acd60-121">-KeyName</span><span class="sxs-lookup"><span data-stu-id="acd60-121">-KeyName</span></span>
<span data-ttu-id="acd60-122">키 자격 증명 모음에서 인증서 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-122">Specifies the name of a certificate key in the key vault.</span></span>

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

### <span data-ttu-id="acd60-123">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="acd60-123">-KeyVaultId</span></span>
<span data-ttu-id="acd60-124">키 보관소 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-124">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="acd60-125">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="acd60-125">-KeyVersion</span></span>
<span data-ttu-id="acd60-126">키 자격 증명 모음의 인증서 키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-126">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="acd60-127">-Metadata</span><span class="sxs-lookup"><span data-stu-id="acd60-127">-Metadata</span></span>
<span data-ttu-id="acd60-128">인증서에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-128">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="acd60-129">-이름</span><span class="sxs-lookup"><span data-stu-id="acd60-129">-Name</span></span>
<span data-ttu-id="acd60-130">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-130">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="acd60-131">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="acd60-131">-PublicCertificateFilePath</span></span>
<span data-ttu-id="acd60-132">공용 인증서 (.cer) 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-132">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="acd60-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="acd60-133">-ResourceGroupName</span></span>
<span data-ttu-id="acd60-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-134">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="acd60-135">-확인</span><span class="sxs-lookup"><span data-stu-id="acd60-135">-Confirm</span></span>
<span data-ttu-id="acd60-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="acd60-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="acd60-137">-WhatIf</span></span>
<span data-ttu-id="acd60-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="acd60-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="acd60-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acd60-140">-DefaultProfile</span></span>
<span data-ttu-id="acd60-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-141">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="acd60-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acd60-142">CommonParameters</span></span>
<span data-ttu-id="acd60-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="acd60-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acd60-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="acd60-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acd60-145">입력</span><span class="sxs-lookup"><span data-stu-id="acd60-145">INPUTS</span></span>

## <span data-ttu-id="acd60-146">출력</span><span class="sxs-lookup"><span data-stu-id="acd60-146">OUTPUTS</span></span>

### <span data-ttu-id="acd60-147">IntegrationAccountCertificate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="acd60-147">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="acd60-148">상속자</span><span class="sxs-lookup"><span data-stu-id="acd60-148">NOTES</span></span>

## <span data-ttu-id="acd60-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="acd60-149">RELATED LINKS</span></span>

[<span data-ttu-id="acd60-150">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="acd60-150">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="acd60-151">새로운 AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="acd60-151">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="acd60-152">제거-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="acd60-152">Remove-AzureRmIntegrationAccountCertificate</span></span>](./Remove-AzureRmIntegrationAccountCertificate.md)


