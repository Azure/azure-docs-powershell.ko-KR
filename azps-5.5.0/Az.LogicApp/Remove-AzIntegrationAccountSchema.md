---
external help file: Microsoft.Azure.PowerShell.Cmdlets.LogicApp.dll-Help.xml
Module Name: Az.LogicApp
ms.assetid: 56550997-21D9-4F85-B23A-677625482547
online version: https://docs.microsoft.com/en-us/powershell/module/az.logicapp/remove-azintegrationaccountschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/LogicApp/LogicApp/help/Remove-AzIntegrationAccountSchema.md
ms.openlocfilehash: 50eab845d20d9bf95c20e94f6309be2a302f413c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100194209"
---
# <span data-ttu-id="0c165-101">Remove-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0c165-101">Remove-AzIntegrationAccountSchema</span></span>

## <span data-ttu-id="0c165-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c165-102">SYNOPSIS</span></span>
<span data-ttu-id="0c165-103">통합 계정 스마마를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-103">Removes an integration account schema.</span></span>

## <span data-ttu-id="0c165-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c165-104">SYNTAX</span></span>

```
Remove-AzIntegrationAccountSchema -ResourceGroupName <String> -Name <String> -SchemaName <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0c165-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c165-105">DESCRIPTION</span></span>
<span data-ttu-id="0c165-106">**Remove-AzIntegrationAccountSchema** cmdlet은 리소스 그룹에서 통합 계정 스마마를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-106">The **Remove-AzIntegrationAccountSchema** cmdlet removes an integration account schema from a resource group.</span></span>
<span data-ttu-id="0c165-107">통합 계정 이름, 리소스 그룹 이름 및 스마마 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-107">Specifying the integration account name, resource group name, and schema name.</span></span>
<span data-ttu-id="0c165-108">이 모듈은 동적 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-108">This module supports dynamic parameters.</span></span>
<span data-ttu-id="0c165-109">동적 매개 변수를 사용 하 고 명령에 입력 합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-109">To use a dynamic parameter, type it in the command.</span></span>
<span data-ttu-id="0c165-110">동적 매개 변수의 이름을 검색하기 위해 cmdlet 이름 다음에 하이픈(-)을 입력한 다음 Tab 키를 반복해서 눌러 사용 가능한 매개 변수를 순환합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-110">To discover the names of dynamic parameters, type a hyphen (-) after the cmdlet name, and then press the Tab key repeatedly to cycle through the available parameters.</span></span>
<span data-ttu-id="0c165-111">필수 템플릿 매개 변수를 생략하면 cmdlet에서 값을 묻는 메시지를 묻습니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-111">If you omit a required template parameter, the cmdlet prompts you for the value.</span></span>

## <span data-ttu-id="0c165-112">예제</span><span class="sxs-lookup"><span data-stu-id="0c165-112">EXAMPLES</span></span>

### <span data-ttu-id="0c165-113">예제 1: 통합 계정 SCHEMA 제거</span><span class="sxs-lookup"><span data-stu-id="0c165-113">Example 1: Remove an integration account schema</span></span>
```
PS C:\>Remove-AzIntegrationAccountSchema -ResourceGroupName "ResourceGroup11" -Name "IntegrationAccount31" -SchemaName "IntegrationAccountSchema43"
```

<span data-ttu-id="0c165-114">이 명령은 IntegrationAccountSchema43이라는 통합 계정 스마마를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-114">This command removes an integration account schema named IntegrationAccountSchema43.</span></span>

## <span data-ttu-id="0c165-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0c165-115">PARAMETERS</span></span>

### <span data-ttu-id="0c165-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c165-116">-DefaultProfile</span></span>
<span data-ttu-id="0c165-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="0c165-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0c165-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0c165-118">-Force</span></span>
<span data-ttu-id="0c165-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="0c165-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0c165-120">-Name</span></span>
<span data-ttu-id="0c165-121">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-121">Specifies the name of the integration account.</span></span>

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

### <span data-ttu-id="0c165-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0c165-122">-ResourceGroupName</span></span>
<span data-ttu-id="0c165-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="0c165-124">-SchemaName</span><span class="sxs-lookup"><span data-stu-id="0c165-124">-SchemaName</span></span>
<span data-ttu-id="0c165-125">통합 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-125">Specifies the name of an integration account schema.</span></span>

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

### <span data-ttu-id="0c165-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0c165-126">-Confirm</span></span>
<span data-ttu-id="0c165-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0c165-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0c165-128">-WhatIf</span></span>
<span data-ttu-id="0c165-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0c165-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0c165-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0c165-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c165-131">CommonParameters</span></span>
<span data-ttu-id="0c165-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c165-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c165-133">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0c165-133">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c165-134">입력</span><span class="sxs-lookup"><span data-stu-id="0c165-134">INPUTS</span></span>

### <span data-ttu-id="0c165-135">System.String</span><span class="sxs-lookup"><span data-stu-id="0c165-135">System.String</span></span>

## <span data-ttu-id="0c165-136">출력</span><span class="sxs-lookup"><span data-stu-id="0c165-136">OUTPUTS</span></span>

### <span data-ttu-id="0c165-137">System.Void</span><span class="sxs-lookup"><span data-stu-id="0c165-137">System.Void</span></span>

## <span data-ttu-id="0c165-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c165-138">NOTES</span></span>

## <span data-ttu-id="0c165-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c165-139">RELATED LINKS</span></span>

[<span data-ttu-id="0c165-140">Get-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0c165-140">Get-AzIntegrationAccountSchema</span></span>](./Get-AzIntegrationAccountSchema.md)

[<span data-ttu-id="0c165-141">New-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0c165-141">New-AzIntegrationAccountSchema</span></span>](./New-AzIntegrationAccountSchema.md)

[<span data-ttu-id="0c165-142">Set-AzIntegrationAccountSchema</span><span class="sxs-lookup"><span data-stu-id="0c165-142">Set-AzIntegrationAccountSchema</span></span>](./Set-AzIntegrationAccountSchema.md)


