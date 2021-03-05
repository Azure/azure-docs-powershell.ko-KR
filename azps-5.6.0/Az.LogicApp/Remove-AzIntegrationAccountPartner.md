---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: E8A557EA-FE3F-4433-BFDE-B4D73DF8467C
online version: https://docs.microsoft.com/powershell/module/az.logicapp/remove-azintegrationaccountpartner
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountPartner.md
ms.openlocfilehash: 4c50f7de3d3748f254d87910fc8c55bb0ba8fc22
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965851"
---
# <span data-ttu-id="ec783-101">Remove-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ec783-101">Remove-AzIntegrationAccountPartner</span></span>

## <span data-ttu-id="ec783-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec783-102">SYNOPSIS</span></span>
<span data-ttu-id="ec783-103">통합 계정 파트너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-103">Removes an integration account partner.</span></span>

## <span data-ttu-id="ec783-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec783-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountPartner -ResourceGroupName <String> -Name <String> -PartnerName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec783-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec783-105">DESCRIPTION</span></span>
<span data-ttu-id="ec783-106">**Remove-AzIntegrationAccountPartner** cmdlet은 리소스 그룹에서 통합 계정 파트너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-106">The **Remove-AzIntegrationAccountPartner** cmdlet removes an integration account partner from a resource group.</span></span>
<span data-ttu-id="ec783-107">통합 계정 이름, 리소스 그룹 이름 및 파트너 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-107">Specify the integration account name, resource group name, and partner name.</span></span>
<span data-ttu-id="ec783-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="ec783-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="ec783-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 뒤 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="ec783-111">필요한 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="ec783-112">예제</span><span class="sxs-lookup"><span data-stu-id="ec783-112">EXAMPLES</span></span>

### <span data-ttu-id="ec783-113">예제 1: 통합 계정 파트너 제거</span><span class="sxs-lookup"><span data-stu-id="ec783-113">Example 1: Remove an integration account partner</span></span>
```
PS C:\>Remove-AzIntegrationAccountPartner -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -PartnerName "IntegrationAccountPartner1"
```

<span data-ttu-id="ec783-114">이 명령은 IntegrationAccountPartner1이라는 통합 계정 파트너를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-114">This command removes the integration account partner named IntegrationAccountPartner1.</span></span>

## <span data-ttu-id="ec783-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec783-115">PARAMETERS</span></span>

### <span data-ttu-id="ec783-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec783-116">-DefaultProfile</span></span>
<span data-ttu-id="ec783-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ec783-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec783-118">-Force</span><span class="sxs-lookup"><span data-stu-id="ec783-118">-Force</span></span>
<span data-ttu-id="ec783-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ec783-120">-Name</span><span class="sxs-lookup"><span data-stu-id="ec783-120">-Name</span></span>
<span data-ttu-id="ec783-121">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-121">Specifies the name of an integration account.</span></span>

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

### <span data-ttu-id="ec783-122">-PartnerName</span><span class="sxs-lookup"><span data-stu-id="ec783-122">-PartnerName</span></span>
<span data-ttu-id="ec783-123">통합 계정 파트너의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-123">Specifies the name of the integration account partner.</span></span>

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

### <span data-ttu-id="ec783-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec783-124">-ResourceGroupName</span></span>
<span data-ttu-id="ec783-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-125">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="ec783-126">-확인</span><span class="sxs-lookup"><span data-stu-id="ec783-126">-Confirm</span></span>
<span data-ttu-id="ec783-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec783-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec783-128">-WhatIf</span></span>
<span data-ttu-id="ec783-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ec783-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec783-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec783-131">CommonParameters</span></span>
<span data-ttu-id="ec783-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec783-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec783-133">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec783-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec783-134">입력</span><span class="sxs-lookup"><span data-stu-id="ec783-134">INPUTS</span></span>

### <span data-ttu-id="ec783-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ec783-135">System.String</span></span>

## <span data-ttu-id="ec783-136">출력</span><span class="sxs-lookup"><span data-stu-id="ec783-136">OUTPUTS</span></span>

### <span data-ttu-id="ec783-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="ec783-137">System.Void</span></span>

## <span data-ttu-id="ec783-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec783-138">NOTES</span></span>

## <span data-ttu-id="ec783-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec783-139">RELATED LINKS</span></span>

[<span data-ttu-id="ec783-140">Get-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ec783-140">Get-AzIntegrationAccountPartner</span></span>](./Get-AzIntegrationAccountPartner.md)

[<span data-ttu-id="ec783-141">New-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ec783-141">New-AzIntegrationAccountPartner</span></span>](./New-AzIntegrationAccountPartner.md)

[<span data-ttu-id="ec783-142">Set-AzIntegrationAccountPartner</span><span class="sxs-lookup"><span data-stu-id="ec783-142">Set-AzIntegrationAccountPartner</span></span>](./Set-AzIntegrationAccountPartner.md)


