---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azinsightsprivatelinkscope
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzInsightsPrivateLinkScope.md
ms.openlocfilehash: 198d52678bceccfd1045522881dc3a62fdebf752
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878477"
---
# <span data-ttu-id="fddf5-101">New-AzInsightsPrivateLinkScope</span><span class="sxs-lookup"><span data-stu-id="fddf5-101">New-AzInsightsPrivateLinkScope</span></span>

## <span data-ttu-id="fddf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fddf5-102">SYNOPSIS</span></span>
<span data-ttu-id="fddf5-103">개인 링크 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="fddf5-103">create private link scope</span></span>

## <span data-ttu-id="fddf5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fddf5-104">SYNTAX</span></span>

```
New-AzInsightsPrivateLinkScope -Location <String> -ResourceGroupName <String> -Name <String> [-Tags <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fddf5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fddf5-105">DESCRIPTION</span></span>
<span data-ttu-id="fddf5-106">개인 링크 범위 만들기</span><span class="sxs-lookup"><span data-stu-id="fddf5-106">create private link scope</span></span>

## <span data-ttu-id="fddf5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fddf5-107">EXAMPLES</span></span>

### <span data-ttu-id="fddf5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fddf5-108">Example 1</span></span>
```powershell
New-AzInsightsPrivateLinkScope -Location "eastus" -ResourceGroupName "rg_name" -Name "scope_name"
```

<span data-ttu-id="fddf5-109">"scope_name" 라는 이름을 가진 개인 링크 범위를 "rg_name" 리소스 그룹의 "" e"" 위치에 "" "로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-109">create private link scope with name "scope_name" under resource group "rg_name" in location "eastus"</span></span>

## <span data-ttu-id="fddf5-110">변수</span><span class="sxs-lookup"><span data-stu-id="fddf5-110">PARAMETERS</span></span>

### <span data-ttu-id="fddf5-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fddf5-111">-DefaultProfile</span></span>
<span data-ttu-id="fddf5-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fddf5-113">-위치</span><span class="sxs-lookup"><span data-stu-id="fddf5-113">-Location</span></span>
<span data-ttu-id="fddf5-114">Location</span><span class="sxs-lookup"><span data-stu-id="fddf5-114">Location</span></span>

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

### <span data-ttu-id="fddf5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="fddf5-115">-Name</span></span>
<span data-ttu-id="fddf5-116">개인 링크 범위 이름</span><span class="sxs-lookup"><span data-stu-id="fddf5-116">Private Link Scope Name</span></span>

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

### <span data-ttu-id="fddf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fddf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="fddf5-118">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fddf5-118">Resource Group Name</span></span>

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

### <span data-ttu-id="fddf5-119">태그</span><span class="sxs-lookup"><span data-stu-id="fddf5-119">-Tags</span></span>
<span data-ttu-id="fddf5-120">태그도</span><span class="sxs-lookup"><span data-stu-id="fddf5-120">Tags</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fddf5-121">-확인</span><span class="sxs-lookup"><span data-stu-id="fddf5-121">-Confirm</span></span>
<span data-ttu-id="fddf5-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fddf5-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fddf5-123">-WhatIf</span></span>
<span data-ttu-id="fddf5-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fddf5-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fddf5-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fddf5-126">CommonParameters</span></span>
<span data-ttu-id="fddf5-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fddf5-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fddf5-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fddf5-129">입력</span><span class="sxs-lookup"><span data-stu-id="fddf5-129">INPUTS</span></span>

### <span data-ttu-id="fddf5-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fddf5-130">System.String</span></span>

## <span data-ttu-id="fddf5-131">출력</span><span class="sxs-lookup"><span data-stu-id="fddf5-131">OUTPUTS</span></span>

### <span data-ttu-id="fddf5-132">PSMonitorPrivateLinkScope를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="fddf5-132">Microsoft.Azure.Commands.Insights.OutputClasses.PSMonitorPrivateLinkScope</span></span>

## <span data-ttu-id="fddf5-133">상속자</span><span class="sxs-lookup"><span data-stu-id="fddf5-133">NOTES</span></span>

## <span data-ttu-id="fddf5-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fddf5-134">RELATED LINKS</span></span>
