---
external help file: Microsoft.Azure.Commands.LogicApp.dll-Help.xml
Module Name: AzureRM.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/LogicApp/Commands.LogicApp/help/Remove-AzureRmIntegrationAccountCertificate.md
ms.openlocfilehash: 71c910fafea0c555f5ba0d7a62573c2de2be3b41
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534032"
---
# <span data-ttu-id="f1702-101">Remove-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f1702-101">Remove-AzureRmIntegrationAccountCertificate</span></span>

## <span data-ttu-id="f1702-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1702-102">SYNOPSIS</span></span>
<span data-ttu-id="f1702-103">리소스 그룹에서 통합 계정 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-103">Removes an integration account certificate from a resource group.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f1702-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f1702-104">SYNTAX</span></span>

```
Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName <String> -Name <String>
 -CertificateName <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f1702-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f1702-105">DESCRIPTION</span></span>
<span data-ttu-id="f1702-106">**AzureRmIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-106">The **Remove-AzureRmIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="f1702-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-107">Specify the integration account name, resource group name, and certificate name.</span></span>

<span data-ttu-id="f1702-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="f1702-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="f1702-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="f1702-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="f1702-112">예제의</span><span class="sxs-lookup"><span data-stu-id="f1702-112">EXAMPLES</span></span>

### <span data-ttu-id="f1702-113">예제 1: 통합 계정 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="f1702-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzureRmIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="f1702-114">이 명령은 IntegrationAccount31 이라는 통합 계정 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="f1702-115">변수</span><span class="sxs-lookup"><span data-stu-id="f1702-115">PARAMETERS</span></span>

### <span data-ttu-id="f1702-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="f1702-116">-CertificateName</span></span>
<span data-ttu-id="f1702-117">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="f1702-118">-Force</span><span class="sxs-lookup"><span data-stu-id="f1702-118">-Force</span></span>
<span data-ttu-id="f1702-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f1702-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f1702-120">-Name</span></span>
<span data-ttu-id="f1702-121">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="f1702-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f1702-122">-ResourceGroupName</span></span>
<span data-ttu-id="f1702-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="f1702-124">-확인</span><span class="sxs-lookup"><span data-stu-id="f1702-124">-Confirm</span></span>
<span data-ttu-id="f1702-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f1702-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1702-126">-WhatIf</span></span>
<span data-ttu-id="f1702-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f1702-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f1702-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1702-129">-DefaultProfile</span></span>
<span data-ttu-id="f1702-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f1702-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1702-131">CommonParameters</span></span>
<span data-ttu-id="f1702-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f1702-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1702-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1702-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1702-134">입력</span><span class="sxs-lookup"><span data-stu-id="f1702-134">INPUTS</span></span>

## <span data-ttu-id="f1702-135">출력</span><span class="sxs-lookup"><span data-stu-id="f1702-135">OUTPUTS</span></span>

## <span data-ttu-id="f1702-136">상속자</span><span class="sxs-lookup"><span data-stu-id="f1702-136">NOTES</span></span>

## <span data-ttu-id="f1702-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1702-137">RELATED LINKS</span></span>

[<span data-ttu-id="f1702-138">Get-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f1702-138">Get-AzureRmIntegrationAccountCertificate</span></span>](./Get-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="f1702-139">새로운 AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f1702-139">New-AzureRmIntegrationAccountCertificate</span></span>](./New-AzureRmIntegrationAccountCertificate.md)

[<span data-ttu-id="f1702-140">Set-AzureRmIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="f1702-140">Set-AzureRmIntegrationAccountCertificate</span></span>](./Set-AzureRmIntegrationAccountCertificate.md)


