---
external help file: Microsoft.Azure.PowerShell.Cmdlets.SignalR.dll-Help.xml
Module Name: Az.SignalR
online version: https://docs.microsoft.com/en-us/powershell/module/az.signalr/new-azsignalrkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/SignalR/SignalR/help/New-AzSignalRKey.md
ms.openlocfilehash: 4bb121563c0fe7a635caeffe982502bff3468495
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93873017"
---
# <span data-ttu-id="f47a3-101">New-AzSignalRKey</span><span class="sxs-lookup"><span data-stu-id="f47a3-101">New-AzSignalRKey</span></span>

## <span data-ttu-id="f47a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f47a3-102">SYNOPSIS</span></span>
<span data-ttu-id="f47a3-103">SignalR 서비스에 대 한 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-103">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f47a3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f47a3-104">SYNTAX</span></span>

### <span data-ttu-id="f47a3-105">ResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f47a3-105">ResourceGroupParameterSet (Default)</span></span>
```
New-AzSignalRKey [-ResourceGroupName <String>] [-Name] <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f47a3-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f47a3-106">ResourceIdParameterSet</span></span>
```
New-AzSignalRKey -ResourceId <String> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f47a3-107">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f47a3-107">InputObjectParameterSet</span></span>
```
New-AzSignalRKey -InputObject <PSSignalRResource> [-KeyType] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47a3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f47a3-108">DESCRIPTION</span></span>
<span data-ttu-id="f47a3-109">SignalR 서비스에 대 한 선택 키를 다시 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-109">Regenerate an access key for a SignalR service.</span></span>

## <span data-ttu-id="f47a3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f47a3-110">EXAMPLES</span></span>

### <span data-ttu-id="f47a3-111">기본 키 다시 생성</span><span class="sxs-lookup"><span data-stu-id="f47a3-111">Regenerate the primary key</span></span>
```powershell
PS C:\> New-AzSignalRKey -ResourceGroupName myResourceGroup -Name mysignalr1 -KeyType Primary -PassThru

True
```

## <span data-ttu-id="f47a3-112">변수</span><span class="sxs-lookup"><span data-stu-id="f47a3-112">PARAMETERS</span></span>

### <span data-ttu-id="f47a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47a3-113">-DefaultProfile</span></span>
<span data-ttu-id="f47a3-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f47a3-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f47a3-115">-InputObject</span></span>
<span data-ttu-id="f47a3-116">SignalR resource 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-116">The SignalR resource object.</span></span>

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

### <span data-ttu-id="f47a3-117">-KeyType</span><span class="sxs-lookup"><span data-stu-id="f47a3-117">-KeyType</span></span>
<span data-ttu-id="f47a3-118">키 형식 (기본 또는 보조)입니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-118">The key type, either Primary or Secondary.</span></span>

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

### <span data-ttu-id="f47a3-119">-이름</span><span class="sxs-lookup"><span data-stu-id="f47a3-119">-Name</span></span>
<span data-ttu-id="f47a3-120">SignalR 서비스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-120">SignalR service name.</span></span>

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

### <span data-ttu-id="f47a3-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f47a3-121">-PassThru</span></span>
<span data-ttu-id="f47a3-122">재생성이 성공적으로 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-122">Returns true if the regeneration was completed successfully.</span></span>

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

### <span data-ttu-id="f47a3-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47a3-123">-ResourceGroupName</span></span>
<span data-ttu-id="f47a3-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-124">Resource group name.</span></span>

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

### <span data-ttu-id="f47a3-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f47a3-125">-ResourceId</span></span>
<span data-ttu-id="f47a3-126">SignalR 서비스 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-126">The SignalR service resource ID.</span></span>

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

### <span data-ttu-id="f47a3-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f47a3-127">-Confirm</span></span>
<span data-ttu-id="f47a3-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f47a3-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47a3-129">-WhatIf</span></span>
<span data-ttu-id="f47a3-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f47a3-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f47a3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47a3-132">CommonParameters</span></span>
<span data-ttu-id="f47a3-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47a3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47a3-134">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f47a3-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47a3-135">입력</span><span class="sxs-lookup"><span data-stu-id="f47a3-135">INPUTS</span></span>

### <span data-ttu-id="f47a3-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f47a3-136">System.String</span></span>
### <span data-ttu-id="f47a3-137">SignalR. PSSignalRResource/.</span><span class="sxs-lookup"><span data-stu-id="f47a3-137">Microsoft.Azure.Commands.SignalR.Models.PSSignalRResource</span></span>
## <span data-ttu-id="f47a3-138">출력</span><span class="sxs-lookup"><span data-stu-id="f47a3-138">OUTPUTS</span></span>

### <span data-ttu-id="f47a3-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f47a3-139">System.Boolean</span></span>
## <span data-ttu-id="f47a3-140">상속자</span><span class="sxs-lookup"><span data-stu-id="f47a3-140">NOTES</span></span>

## <span data-ttu-id="f47a3-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f47a3-141">RELATED LINKS</span></span>
