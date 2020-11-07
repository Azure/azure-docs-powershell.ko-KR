---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F9871519-F470-470C-8CCE-A674B6B5A3EE
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountCertificate.md
ms.openlocfilehash: 9e857d506b149c79d86ca52f2d3d7d3e3d598216
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689494"
---
# <span data-ttu-id="46e43-101">Remove-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="46e43-101">Remove-AzIntegrationAccountCertificate</span></span>

## <span data-ttu-id="46e43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e43-102">SYNOPSIS</span></span>
<span data-ttu-id="46e43-103">리소스 그룹에서 통합 계정 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-103">Removes an integration account certificate from a resource group.</span></span>

## <span data-ttu-id="46e43-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46e43-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountCertificate -ResourceGroupName <String> -Name <String> -CertificateName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="46e43-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46e43-105">DESCRIPTION</span></span>
<span data-ttu-id="46e43-106">**AzIntegrationAccountCertificate** cmdlet은 리소스 그룹에서 통합 계정 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-106">The **Remove-AzIntegrationAccountCertificate** cmdlet removes an integration account certificate from a resource group.</span></span>
<span data-ttu-id="46e43-107">통합 계정 이름, 리소스 그룹 이름 및 인증서 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-107">Specify the integration account name, resource group name, and certificate name.</span></span>
<span data-ttu-id="46e43-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="46e43-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="46e43-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="46e43-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="46e43-112">예제의</span><span class="sxs-lookup"><span data-stu-id="46e43-112">EXAMPLES</span></span>

### <span data-ttu-id="46e43-113">예제 1: 통합 계정 인증서 제거</span><span class="sxs-lookup"><span data-stu-id="46e43-113">Example 1: Remove an integration account certificate</span></span>
```
PS C:\>Remove-AzIntegrationAccountCertificate -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -CertificateName "IntegrationAccountCertificate01"
```

<span data-ttu-id="46e43-114">이 명령은 IntegrationAccount31 이라는 통합 계정 인증서를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-114">This command removes the integration account certificate named IntegrationAccount31.</span></span>

## <span data-ttu-id="46e43-115">변수</span><span class="sxs-lookup"><span data-stu-id="46e43-115">PARAMETERS</span></span>

### <span data-ttu-id="46e43-116">-CertificateName</span><span class="sxs-lookup"><span data-stu-id="46e43-116">-CertificateName</span></span>
<span data-ttu-id="46e43-117">통합 계정 인증서의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-117">Specifies the name of an integration account certificate.</span></span>

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

### <span data-ttu-id="46e43-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e43-118">-DefaultProfile</span></span>
<span data-ttu-id="46e43-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="46e43-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="46e43-120">-Force</span><span class="sxs-lookup"><span data-stu-id="46e43-120">-Force</span></span>
<span data-ttu-id="46e43-121">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-121">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="46e43-122">-이름</span><span class="sxs-lookup"><span data-stu-id="46e43-122">-Name</span></span>
<span data-ttu-id="46e43-123">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-123">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="46e43-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46e43-124">-ResourceGroupName</span></span>
<span data-ttu-id="46e43-125">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="46e43-126">-확인</span><span class="sxs-lookup"><span data-stu-id="46e43-126">-Confirm</span></span>
<span data-ttu-id="46e43-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="46e43-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="46e43-128">-WhatIf</span></span>
<span data-ttu-id="46e43-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="46e43-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="46e43-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e43-131">CommonParameters</span></span>
<span data-ttu-id="46e43-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e43-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e43-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46e43-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e43-134">입력</span><span class="sxs-lookup"><span data-stu-id="46e43-134">INPUTS</span></span>

### <span data-ttu-id="46e43-135">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46e43-135">System.String</span></span>

## <span data-ttu-id="46e43-136">출력</span><span class="sxs-lookup"><span data-stu-id="46e43-136">OUTPUTS</span></span>

### <span data-ttu-id="46e43-137">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="46e43-137">System.Void</span></span>

## <span data-ttu-id="46e43-138">상속자</span><span class="sxs-lookup"><span data-stu-id="46e43-138">NOTES</span></span>

## <span data-ttu-id="46e43-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46e43-139">RELATED LINKS</span></span>

[<span data-ttu-id="46e43-140">Get-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="46e43-140">Get-AzIntegrationAccountCertificate</span></span>](./Get-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="46e43-141">새로운 AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="46e43-141">New-AzIntegrationAccountCertificate</span></span>](./New-AzIntegrationAccountCertificate.md)

[<span data-ttu-id="46e43-142">Set-AzIntegrationAccountCertificate</span><span class="sxs-lookup"><span data-stu-id="46e43-142">Set-AzIntegrationAccountCertificate</span></span>](./Set-AzIntegrationAccountCertificate.md)


