---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: BB1B49CD-B42F-4222-B0BA-0AA4CE3C95E0
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/new-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/New-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 651ce1141e9a925d5571f8b70d8eecedb4a1e66d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218969"
---
# <span data-ttu-id="3b751-101">New-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3b751-101">New-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="3b751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b751-102">SYNOPSIS</span></span>
<span data-ttu-id="3b751-103">통합 계정 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-103">Creates an integration account certificate.</span></span>

## <span data-ttu-id="3b751-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3b751-104">SYNTAX</span></span>

### <span data-ttu-id="3b751-105">PrivateKey</span><span class="sxs-lookup"><span data-stu-id="3b751-105">PrivateKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> [-PublicCertificateFilePath <String>]
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b751-106">PublicKey</span><span class="sxs-lookup"><span data-stu-id="3b751-106">PublicKey</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-KeyName <String>] [-KeyVersion <String>] [-KeyVaultId <String>] -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b751-107">양방향</span><span class="sxs-lookup"><span data-stu-id="3b751-107">Both</span></span>
```
New-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 -KeyName <String> -KeyVersion <String> -KeyVaultId <String> -PublicCertificateFilePath <String>
 [-Metadata <Object>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b751-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3b751-108">DESCRIPTION</span></span>
<span data-ttu-id="3b751-109">**새 AzIntegrationAccountCertificate** cmdlet은 통합 계정 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-109">The **New-AzIntegrationAccountCertificate** cmdlet creates an integration account certificate.</span></span>
<span data-ttu-id="3b751-110">이 cmdlet은 통합 계정 인증서를 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-110">This cmdlet returns an object that represents the integration account certificate.</span></span>
<span data-ttu-id="3b751-111">통합 계정 이름, 리소스 그룹 이름, 인증서 이름, 키 이름, 키 버전, 키 자격 증명 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-111">Specify the integration account name, resource group name, certificate name, key name, key version, and key vault ID.</span></span>
<span data-ttu-id="3b751-112">명령줄에서 지정한 템플릿 매개 변수 파일 값이 템플릿 매개 변수 개체의 템플릿 매개 변수 값 보다 우선 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-112">Template parameter file values that you specify at the command line take precedence over template parameter values in a template parameter object.</span></span>
<span data-ttu-id="3b751-113">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-113">This module supports dynamic parameters.</span></span>
<span data-ttu-id="3b751-114">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-114">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="3b751-115">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-115">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="3b751-116">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-116">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="3b751-117">예제의</span><span class="sxs-lookup"><span data-stu-id="3b751-117">EXAMPLES</span></span>

### <span data-ttu-id="3b751-118">예제 1: 통합 계정 인증서 만들기</span><span class="sxs-lookup"><span data-stu-id="3b751-118">Example 1: Create an integration account certificate</span></span>
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

<span data-ttu-id="3b751-119">이 명령은 지정 된 리소스 그룹에 통합 계정 인증서를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-119">This command creates the integration account certificate in the specified resource group.</span></span>

## <span data-ttu-id="3b751-120">변수</span><span class="sxs-lookup"><span data-stu-id="3b751-120">PARAMETERS</span></span>

### <span data-ttu-id="3b751-121">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="3b751-121">-CertificateName</span></span>
<span data-ttu-id="3b751-122">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-122">Specifies a name for the integration account certificate.</span></span>

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

### <span data-ttu-id="3b751-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b751-123">-DefaultProfile</span></span>
<span data-ttu-id="3b751-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3b751-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3b751-125">-KeyName</span><span class="sxs-lookup"><span data-stu-id="3b751-125">-KeyName</span></span>
<span data-ttu-id="3b751-126">키 자격 증명 모음에서 인증서 키의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-126">Specifies the name of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="3b751-127">-KeyVaultId</span><span class="sxs-lookup"><span data-stu-id="3b751-127">-KeyVaultId</span></span>
<span data-ttu-id="3b751-128">키 보관소 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-128">Specifies a key vault ID.</span></span>

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

### <span data-ttu-id="3b751-129">-KeyVersion</span><span class="sxs-lookup"><span data-stu-id="3b751-129">-KeyVersion</span></span>
<span data-ttu-id="3b751-130">키 자격 증명 모음의 인증서 키 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-130">Specifies the version of the certificate key in the key vault.</span></span>

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

### <span data-ttu-id="3b751-131">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3b751-131">-Metadata</span></span>
<span data-ttu-id="3b751-132">인증서에 대 한 메타 데이터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-132">Specifies a metadata object for the certificate.</span></span>

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

### <span data-ttu-id="3b751-133">-이름</span><span class="sxs-lookup"><span data-stu-id="3b751-133">-Name</span></span>
<span data-ttu-id="3b751-134">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-134">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="3b751-135">-PublicCertificateFilePath</span><span class="sxs-lookup"><span data-stu-id="3b751-135">-PublicCertificateFilePath</span></span>
<span data-ttu-id="3b751-136">공용 인증서 (.cer) 파일의 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-136">Specifies the path of a public certificate (.cer) file.</span></span>

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

### <span data-ttu-id="3b751-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3b751-137">-ResourceGroupName</span></span>
<span data-ttu-id="3b751-138">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-138">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="3b751-139">-확인</span><span class="sxs-lookup"><span data-stu-id="3b751-139">-Confirm</span></span>
<span data-ttu-id="3b751-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b751-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b751-141">-WhatIf</span></span>
<span data-ttu-id="3b751-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b751-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b751-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b751-144">CommonParameters</span></span>
<span data-ttu-id="3b751-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3b751-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b751-146">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b751-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b751-147">입력</span><span class="sxs-lookup"><span data-stu-id="3b751-147">INPUTS</span></span>

### <span data-ttu-id="3b751-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3b751-148">System.String</span></span>

## <span data-ttu-id="3b751-149">출력</span><span class="sxs-lookup"><span data-stu-id="3b751-149">OUTPUTS</span></span>

### <span data-ttu-id="3b751-150">IntegrationAccountCertificate를 통해 관리 되는 모델</span><span class="sxs-lookup"><span data-stu-id="3b751-150">Microsoft.Azure.Management.Logic.Models.IntegrationAccountCertificate</span></span>

## <span data-ttu-id="3b751-151">상속자</span><span class="sxs-lookup"><span data-stu-id="3b751-151">NOTES</span></span>

## <span data-ttu-id="3b751-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3b751-152">RELATED LINKS</span></span>

[<span data-ttu-id="3b751-153">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3b751-153">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="3b751-154">제거-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3b751-154">Remove-AzIntegrationAccountCertificate</span></span>](./Remove-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="3b751-155">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="3b751-155">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


