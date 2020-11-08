---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 9c27342a073f33a52881376037fc8d3a5d7e8bb1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034749"
---
# <span data-ttu-id="3a139-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="3a139-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="3a139-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a139-102">SYNOPSIS</span></span>
<span data-ttu-id="3a139-103">SignalR 서비스에 대 한 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="3a139-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a139-104">SYNTAX</span></span>

### <span data-ttu-id="3a139-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a139-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a139-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a139-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a139-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a139-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a139-108">설명은</span><span class="sxs-lookup"><span data-stu-id="3a139-108">DESCRIPTION</span></span>
<span data-ttu-id="3a139-109">SignalR 서비스에 대 한 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="3a139-110">예제의</span><span class="sxs-lookup"><span data-stu-id="3a139-110">EXAMPLES</span></span>

### <span data-ttu-id="3a139-111">기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="3a139-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="3a139-112">변수</span><span class="sxs-lookup"><span data-stu-id="3a139-112">PARAMETERS</span></span>

### <span data-ttu-id="3a139-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a139-113">-DefaultProfile</span></span>
<span data-ttu-id="3a139-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a139-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3a139-115">-InputObject</span></span>
<span data-ttu-id="3a139-116">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-116">The SignalR resource object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a139-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="3a139-117">-KeyType</span></span>
<span data-ttu-id="3a139-118">키 형식 (기본 또는 보조)입니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-118">The key type, either Primary or Secondary.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Primary, Secondary

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a139-119">-이름</span><span class="sxs-lookup"><span data-stu-id="3a139-119">-Name</span></span>
<span data-ttu-id="3a139-120">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-120">SignalR service name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a139-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="3a139-121">-PassThru</span></span>
<span data-ttu-id="3a139-122">재생성이 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="3a139-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a139-123">-ResourceGroupName</span></span>
<span data-ttu-id="3a139-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-124">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a139-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3a139-125">-ResourceId</span></span>
<span data-ttu-id="3a139-126">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-126">The SignalR service resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3a139-127">-확인</span><span class="sxs-lookup"><span data-stu-id="3a139-127">-Confirm</span></span>
<span data-ttu-id="3a139-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a139-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a139-129">-WhatIf</span></span>
<span data-ttu-id="3a139-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a139-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a139-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a139-132">CommonParameters</span></span>
<span data-ttu-id="3a139-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a139-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a139-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a139-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a139-135">입력</span><span class="sxs-lookup"><span data-stu-id="3a139-135">INPUTS</span></span>

### <span data-ttu-id="3a139-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3a139-136">System.String</span></span>
### <span data-ttu-id="3a139-137">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="3a139-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="3a139-138">출력</span><span class="sxs-lookup"><span data-stu-id="3a139-138">OUTPUTS</span></span>

### <span data-ttu-id="3a139-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="3a139-139">System.Boolean</span></span>
## <span data-ttu-id="3a139-140">상속자</span><span class="sxs-lookup"><span data-stu-id="3a139-140">NOTES</span></span>

## <span data-ttu-id="3a139-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a139-141">RELATED LINKS</span></span>
