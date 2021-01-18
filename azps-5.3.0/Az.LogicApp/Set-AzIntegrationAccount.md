---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: F6D9EA59-BA61-4117-8771-9B190424BFF8
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/set-azintegrationaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Set-AzIntegrationAccount.md
ms.openlocfilehash: 3bb20e0314e95f2586c0bd8585c7937c4d6ca5b3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492832"
---
# <span data-ttu-id="8aa92-101">Set-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8aa92-101">Set-AzIntegrationAccount</span></span>

## <span data-ttu-id="8aa92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8aa92-102">SYNOPSIS</span></span>
<span data-ttu-id="8aa92-103">통합 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-103">Modifies an integration account.</span></span>

## <span data-ttu-id="8aa92-104">구문</span><span class="sxs-lookup"><span data-stu-id="8aa92-104">SYNTAX</span></span>

```
Set-AzIntegrationAccount -ResourceGroupName <String> -Name <String> [-Location <String>] [-Sku <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8aa92-105">설명</span><span class="sxs-lookup"><span data-stu-id="8aa92-105">DESCRIPTION</span></span>
<span data-ttu-id="8aa92-106">**Set-AzIntegrationAccount** cmdlet은 통합 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-106">The **Set-AzIntegrationAccount** cmdlet modifies an integration account.</span></span>
<span data-ttu-id="8aa92-107">이 cmdlet은 통합 계정을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-107">This cmdlet returns an object that represents the integration account.</span></span>
<span data-ttu-id="8aa92-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="8aa92-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="8aa92-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="8aa92-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="8aa92-112">예제</span><span class="sxs-lookup"><span data-stu-id="8aa92-112">EXAMPLES</span></span>

### <span data-ttu-id="8aa92-113">예제 1: 통합 계정 수정</span><span class="sxs-lookup"><span data-stu-id="8aa92-113">Example 1: Modify an integration account</span></span>
```
PS C:\>Set-AzIntegrationAccount -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -Sku "Free"
Id          : /subscriptions/<SubscriptionId>/resourceGroups/ResourceGroup11/providers/Microsoft.Logic/integrationAccounts/IntegrationAccount31
Name        : IntegrationAccount31
Type        : Microsoft.Logic/integrationAccounts
Location    : brazilsouth
Sku         : 
CreatedTime : 3/26/2016 4:26:07 PM
ChangedTime : 3/26/2016 4:26:07 PM
```

<span data-ttu-id="8aa92-114">이 명령은 지정된 리소스 그룹에서 IntegrationAccount31이라는 통합 계정을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-114">This command modifies an integration account named IntegrationAccount31 in the specified resource group.</span></span>

## <span data-ttu-id="8aa92-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8aa92-115">PARAMETERS</span></span>

### <span data-ttu-id="8aa92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8aa92-116">-DefaultProfile</span></span>
<span data-ttu-id="8aa92-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8aa92-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8aa92-118">-Force</span><span class="sxs-lookup"><span data-stu-id="8aa92-118">-Force</span></span>
<span data-ttu-id="8aa92-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="8aa92-120">-Location</span><span class="sxs-lookup"><span data-stu-id="8aa92-120">-Location</span></span>
<span data-ttu-id="8aa92-121">통합 계정의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-121">Specifies a location for the integration account.</span></span>

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

### <span data-ttu-id="8aa92-122">-Name</span><span class="sxs-lookup"><span data-stu-id="8aa92-122">-Name</span></span>
<span data-ttu-id="8aa92-123">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-123">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="8aa92-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8aa92-124">-ResourceGroupName</span></span>
<span data-ttu-id="8aa92-125">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-125">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="8aa92-126">-Sku</span><span class="sxs-lookup"><span data-stu-id="8aa92-126">-Sku</span></span>
<span data-ttu-id="8aa92-127">통합 계정에 대한 SKU 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-127">Specifies a SKU name for the integration account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Free, Basic, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8aa92-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="8aa92-128">-Confirm</span></span>
<span data-ttu-id="8aa92-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8aa92-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8aa92-130">-WhatIf</span></span>
<span data-ttu-id="8aa92-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="8aa92-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8aa92-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8aa92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8aa92-133">CommonParameters</span></span>
<span data-ttu-id="8aa92-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8aa92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8aa92-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8aa92-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8aa92-136">입력</span><span class="sxs-lookup"><span data-stu-id="8aa92-136">INPUTS</span></span>

### <span data-ttu-id="8aa92-137">System.String</span><span class="sxs-lookup"><span data-stu-id="8aa92-137">System.String</span></span>

## <span data-ttu-id="8aa92-138">출력</span><span class="sxs-lookup"><span data-stu-id="8aa92-138">OUTPUTS</span></span>

### <span data-ttu-id="8aa92-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8aa92-139">Microsoft.Azure.Management.Logic.Models.IntegrationAccount</span></span>

## <span data-ttu-id="8aa92-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8aa92-140">NOTES</span></span>

## <span data-ttu-id="8aa92-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8aa92-141">RELATED LINKS</span></span>

[<span data-ttu-id="8aa92-142">Get-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8aa92-142">Get-AzIntegrationAccount</span></span>](./Get-AzIntegrationAccount.md)

[<span data-ttu-id="8aa92-143">New-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8aa92-143">New-AzIntegrationAccount</span></span>](./New-AzIntegrationAccount.md)

[<span data-ttu-id="8aa92-144">Remove-AzIntegrationAccount</span><span class="sxs-lookup"><span data-stu-id="8aa92-144">Remove-AzIntegrationAccount</span></span>](./Remove-AzIntegrationAccount.md)


