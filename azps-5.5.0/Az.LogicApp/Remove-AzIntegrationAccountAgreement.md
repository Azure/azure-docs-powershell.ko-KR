---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: EBDBB9F0-CA2E-4E4F-9034-3D0FAB88E442
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountagreement
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountAgreement.md
ms.openlocfilehash: 3ae5a1511cfab243e1454242d276af463c542fc5
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194212"
---
# <span data-ttu-id="bf133-101">Remove-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bf133-101">Remove-AzIntegrationAccountAgreement</span></span>

## <span data-ttu-id="bf133-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf133-102">SYNOPSIS</span></span>
<span data-ttu-id="bf133-103">통합 계정 계약을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-103">Removes an integration account agreement.</span></span>

## <span data-ttu-id="bf133-104">구문</span><span class="sxs-lookup"><span data-stu-id="bf133-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountAgreement -ResourceGroupName <String> -Name <String> -AgreementName <String>
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bf133-105">설명</span><span class="sxs-lookup"><span data-stu-id="bf133-105">DESCRIPTION</span></span>
<span data-ttu-id="bf133-106">**Remove-AzIntegrationAccountAgreement** cmdlet은 Azure 리소스 그룹에서 통합 계정 계약을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-106">The **Remove-AzIntegrationAccountAgreement** cmdlet removes an integration account agreement from an Azure resource group.</span></span>
<span data-ttu-id="bf133-107">통합 계정 이름, 리소스 그룹 이름 및 계약 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-107">Specify the integration account name, resource group name, and agreement name.</span></span>
<span data-ttu-id="bf133-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="bf133-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="bf133-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="bf133-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="bf133-112">예제</span><span class="sxs-lookup"><span data-stu-id="bf133-112">EXAMPLES</span></span>

### <span data-ttu-id="bf133-113">예제 1: 이름에 따라 통합 계정 계약 제거</span><span class="sxs-lookup"><span data-stu-id="bf133-113">Example 1: Remove an integration account agreement by name</span></span>
```
PS C:\>Remove-AzIntegrationAccountAgreement -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -AgreementName "IntegrationAccountAgreement06" -Force
```

<span data-ttu-id="bf133-114">이 명령은 IntegrationAccountAgreement06이라는 통합 계정 계약을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-114">This command removes the integration account agreement named IntegrationAccountAgreement06.</span></span>
<span data-ttu-id="bf133-115">이 명령은 확인을 요청하는 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-115">The command does not prompt you for confirmation.</span></span>

## <span data-ttu-id="bf133-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="bf133-116">PARAMETERS</span></span>

### <span data-ttu-id="bf133-117">-AgreementName</span><span class="sxs-lookup"><span data-stu-id="bf133-117">-AgreementName</span></span>
<span data-ttu-id="bf133-118">통합 계정 계약의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-118">Specifies the name of the integration account agreement.</span></span>

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

### <span data-ttu-id="bf133-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bf133-119">-DefaultProfile</span></span>
<span data-ttu-id="bf133-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bf133-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bf133-121">-Force</span><span class="sxs-lookup"><span data-stu-id="bf133-121">-Force</span></span>
<span data-ttu-id="bf133-122">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="bf133-123">-Name</span><span class="sxs-lookup"><span data-stu-id="bf133-123">-Name</span></span>
<span data-ttu-id="bf133-124">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-124">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="bf133-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bf133-125">-ResourceGroupName</span></span>
<span data-ttu-id="bf133-126">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-126">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="bf133-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="bf133-127">-Confirm</span></span>
<span data-ttu-id="bf133-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bf133-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bf133-129">-WhatIf</span></span>
<span data-ttu-id="bf133-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="bf133-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bf133-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bf133-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf133-132">CommonParameters</span></span>
<span data-ttu-id="bf133-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bf133-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf133-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="bf133-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf133-135">입력</span><span class="sxs-lookup"><span data-stu-id="bf133-135">INPUTS</span></span>

### <span data-ttu-id="bf133-136">System.String</span><span class="sxs-lookup"><span data-stu-id="bf133-136">System.String</span></span>

## <span data-ttu-id="bf133-137">출력</span><span class="sxs-lookup"><span data-stu-id="bf133-137">OUTPUTS</span></span>

### <span data-ttu-id="bf133-138">System.Void</span><span class="sxs-lookup"><span data-stu-id="bf133-138">System.Void</span></span>

## <span data-ttu-id="bf133-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bf133-139">NOTES</span></span>

## <span data-ttu-id="bf133-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf133-140">RELATED LINKS</span></span>

[<span data-ttu-id="bf133-141">Get-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bf133-141">Get-AzIntegrationAccountAgreement</span></span>](./Get-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="bf133-142">New-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bf133-142">New-AzIntegrationAccountAgreement</span></span>](./New-AzIntegrationAccountAgreement.md)

[<span data-ttu-id="bf133-143">Set-AzIntegrationAccountAgreement</span><span class="sxs-lookup"><span data-stu-id="bf133-143">Set-AzIntegrationAccountAgreement</span></span>](./Set-AzIntegrationAccountAgreement.md)


