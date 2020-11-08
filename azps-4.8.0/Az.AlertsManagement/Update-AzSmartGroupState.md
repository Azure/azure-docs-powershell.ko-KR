---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AlertsManagement.dll-Help.xml
Module Name: Az.AlertsManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.alertsmanagement/update-azsmartgroupstate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AlertsManagement/AlertsManagement/help/Update-AzSmartGroupState.md
ms.openlocfilehash: 6c0b67bb70a364de45a88f80ca99bdec5e1d7188
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048024"
---
# <span data-ttu-id="d5187-101">Update-AzSmartGroupState</span><span class="sxs-lookup"><span data-stu-id="d5187-101">Update-AzSmartGroupState</span></span>

## <span data-ttu-id="d5187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5187-102">SYNOPSIS</span></span>
<span data-ttu-id="d5187-103">스마트 그룹 상태 업데이트</span><span class="sxs-lookup"><span data-stu-id="d5187-103">Updates smart group state</span></span>

## <span data-ttu-id="d5187-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d5187-104">SYNTAX</span></span>

### <span data-ttu-id="d5187-105">BySmartGroupId (기본값)</span><span class="sxs-lookup"><span data-stu-id="d5187-105">BySmartGroupId (Default)</span></span>
```
Update-AzSmartGroupState -SmartGroupId <String> -State <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d5187-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="d5187-106">ByInputObject</span></span>
```
Update-AzSmartGroupState -State <String> -InputObject <PSSmartGroup> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d5187-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d5187-107">DESCRIPTION</span></span>
<span data-ttu-id="d5187-108">**업데이트-AzSmartGroupState cmdlet은** 스마트 그룹 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-108">**Update-AzSmartGroupState** cmdlet updates smart group state.</span></span>

## <span data-ttu-id="d5187-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d5187-109">EXAMPLES</span></span>

### <span data-ttu-id="d5187-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="d5187-110">Example 1</span></span>
```powershell
PS C:\> Update-AzSmartGroupState -SmartGroupId "afbf1b3a-0a6c-4f19-9c9b-644ccd7b1529" -State "Acknowledged"
```

<span data-ttu-id="d5187-111">이 cmdlet은 스마트 그룹 상태를 Acknowleged로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-111">This cmdlet updates the smart group state to Acknowleged.</span></span>

## <span data-ttu-id="d5187-112">변수</span><span class="sxs-lookup"><span data-stu-id="d5187-112">PARAMETERS</span></span>

### <span data-ttu-id="d5187-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5187-113">-DefaultProfile</span></span>
<span data-ttu-id="d5187-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5187-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d5187-115">-InputObject</span></span>
<span data-ttu-id="d5187-116">파이프라인의 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-116">Input object from pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d5187-117">-SmartGroupId</span><span class="sxs-lookup"><span data-stu-id="d5187-117">-SmartGroupId</span></span>
<span data-ttu-id="d5187-118">스마트 그룹의 스마트 그룹 ResourceId에 대 한 고유 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-118">Unique Identifier of Smart Group / ResourceId of smart group.</span></span>

```yaml
Type: System.String
Parameter Sets: BySmartGroupId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5187-119">-상태</span><span class="sxs-lookup"><span data-stu-id="d5187-119">-State</span></span>
<span data-ttu-id="d5187-120">스마트 그룹 상태 업데이트</span><span class="sxs-lookup"><span data-stu-id="d5187-120">Updated Smart group State</span></span>

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

### <span data-ttu-id="d5187-121">-확인</span><span class="sxs-lookup"><span data-stu-id="d5187-121">-Confirm</span></span>
<span data-ttu-id="d5187-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5187-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d5187-123">-WhatIf</span></span>
<span data-ttu-id="d5187-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d5187-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5187-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5187-126">CommonParameters</span></span>
<span data-ttu-id="d5187-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d5187-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5187-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d5187-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5187-129">입력</span><span class="sxs-lookup"><span data-stu-id="d5187-129">INPUTS</span></span>

### <span data-ttu-id="d5187-130">않아야</span><span class="sxs-lookup"><span data-stu-id="d5187-130">None</span></span>

## <span data-ttu-id="d5187-131">출력</span><span class="sxs-lookup"><span data-stu-id="d5187-131">OUTPUTS</span></span>

### <span data-ttu-id="d5187-132">AlertsManagement 모델. a PSSmartGroup</span><span class="sxs-lookup"><span data-stu-id="d5187-132">Microsoft.Azure.Commands.AlertsManagement.OutputModels.PSSmartGroup</span></span>

## <span data-ttu-id="d5187-133">상속자</span><span class="sxs-lookup"><span data-stu-id="d5187-133">NOTES</span></span>

## <span data-ttu-id="d5187-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d5187-134">RELATED LINKS</span></span>
