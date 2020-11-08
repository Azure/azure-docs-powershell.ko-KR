---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226851"
---
# <span data-ttu-id="78860-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="78860-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="78860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78860-102">SYNOPSIS</span></span>
<span data-ttu-id="78860-103">통합 계정 계약을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="78860-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78860-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78860-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78860-105">DESCRIPTION</span></span>
<span data-ttu-id="78860-106">**AzIntegrationAccountAgreement** Cmdlet는 Azure 리소스 그룹의 통합 계정 계약을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="78860-107">통합 계정 이름, 리소스 그룹 이름 및 규약 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="78860-108">이 모듈은 동적 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="78860-109">동적 매개 변수를 사용 하려면 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="78860-110">동적 매개 변수의 이름을 검색 하려면 cmdlet 이름 뒤에 하이픈 (-)을 입력 한 다음 Tab 키를 반복적으로 눌러 사용할 수 있는 매개 변수를 순환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="78860-111">필수 템플릿 매개 변수를 생략 하면 cmdlet에서 값을 묻는 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="78860-112">예제의</span><span class="sxs-lookup"><span data-stu-id="78860-112">EXAMPLES</span></span>

### <span data-ttu-id="78860-113">예제 1: 이름별 통합 계정 계약 제거</span><span class="sxs-lookup"><span data-stu-id="78860-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="78860-114">이 명령은 IntegrationAccountAgreement06 이라는 통합 계정 계약을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="78860-115">명령에 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78860-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="78860-116">변수</span><span class="sxs-lookup"><span data-stu-id="78860-116">PARAMETERS</span></span>

### <span data-ttu-id="78860-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="78860-117">-AgreementName</span></span>
<span data-ttu-id="78860-118">통합 계정 계약의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="78860-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78860-119">-DefaultProfile</span></span>
<span data-ttu-id="78860-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78860-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78860-121">-Force</span><span class="sxs-lookup"><span data-stu-id="78860-121">-Force</span></span>
<span data-ttu-id="78860-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="78860-123">-이름</span><span class="sxs-lookup"><span data-stu-id="78860-123">-Name</span></span>
<span data-ttu-id="78860-124">통합 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="78860-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78860-125">-ResourceGroupName</span></span>
<span data-ttu-id="78860-126">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="78860-127">-확인</span><span class="sxs-lookup"><span data-stu-id="78860-127">-Confirm</span></span>
<span data-ttu-id="78860-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78860-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78860-129">-WhatIf</span></span>
<span data-ttu-id="78860-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78860-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78860-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78860-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78860-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78860-132">CommonParameters</span></span>
<span data-ttu-id="78860-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78860-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78860-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78860-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78860-135">입력</span><span class="sxs-lookup"><span data-stu-id="78860-135">INPUTS</span></span>

### <span data-ttu-id="78860-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78860-136">System.String</span></span>

## <span data-ttu-id="78860-137">출력</span><span class="sxs-lookup"><span data-stu-id="78860-137">OUTPUTS</span></span>

### <span data-ttu-id="78860-138">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="78860-138">System.Void</span></span>

## <span data-ttu-id="78860-139">상속자</span><span class="sxs-lookup"><span data-stu-id="78860-139">NOTES</span></span>

## <span data-ttu-id="78860-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78860-140">RELATED LINKS</span></span>

[<span data-ttu-id="78860-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="78860-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="78860-142">새로운 AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="78860-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="78860-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="78860-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


