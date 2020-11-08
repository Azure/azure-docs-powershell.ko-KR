---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Peering.dll-Help.xml
Module Name: Az.Peering
online version: https://docs.microsoft.com/en-us/powershell/module/az.peering/set-azpeeringregisteredprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Peering/Peering/help/Set-AzPeeringRegisteredPrefix.md
ms.openlocfilehash: 83d36cfdb892cc5366aabb589f3536e18e79eace
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212932"
---
# <span data-ttu-id="07542-101">Set-AzPeeringRegisteredPrefix</span><span class="sxs-lookup"><span data-stu-id="07542-101">Set-AzPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="07542-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07542-102">SYNOPSIS</span></span>
<span data-ttu-id="07542-103">부모 피어 링 리소스에서 등록 된 접두사를 설정 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-103">Sets or updates a registered prefix from the parent peering resource.</span></span>

## <span data-ttu-id="07542-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07542-104">SYNTAX</span></span>

### <span data-ttu-id="07542-105">ByResourceGroupAndName (기본값)</span><span class="sxs-lookup"><span data-stu-id="07542-105">ByResourceGroupAndName (Default)</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceGroupName] <String> [-PeeringName] <String> [-Name] <String>
 -Prefix <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07542-106">InputObject</span><span class="sxs-lookup"><span data-stu-id="07542-106">InputObject</span></span>
```
Set-AzPeeringRegisteredPrefix -InputObject <PSPeeringRegisteredPrefix> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07542-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="07542-107">ByResourceId</span></span>
```
Set-AzPeeringRegisteredPrefix [-ResourceId] <String> [-Name] <String> -Prefix <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07542-108">설명은</span><span class="sxs-lookup"><span data-stu-id="07542-108">DESCRIPTION</span></span>
<span data-ttu-id="07542-109">부모 피어 링 리소스에서 등록 된 접두사의 업데이트를 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-109">Allows the updating of a registered prefix from parent peering resource.</span></span>

## <span data-ttu-id="07542-110">예제의</span><span class="sxs-lookup"><span data-stu-id="07542-110">EXAMPLES</span></span>

### <span data-ttu-id="07542-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="07542-111">Example 1</span></span>
```powershell
PS C:\> Set-AzPeeringRegisteredPrefix -ResourceId $resourceId -Prefix $newPrefix
```

<span data-ttu-id="07542-112">리소스 id를 기준으로 접두사를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-112">Updates the prefix by resource id.</span></span>

## <span data-ttu-id="07542-113">변수</span><span class="sxs-lookup"><span data-stu-id="07542-113">PARAMETERS</span></span>

### <span data-ttu-id="07542-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07542-114">-AsJob</span></span>
<span data-ttu-id="07542-115">백그라운드에서 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-115">Run in the background.</span></span>

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

### <span data-ttu-id="07542-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07542-116">-DefaultProfile</span></span>
<span data-ttu-id="07542-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07542-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="07542-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="07542-118">-InputObject</span></span>
<span data-ttu-id="07542-119">Get-AzPeering 사용</span><span class="sxs-lookup"><span data-stu-id="07542-119">Use a Get-AzPeering</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="07542-120">-이름</span><span class="sxs-lookup"><span data-stu-id="07542-120">-Name</span></span>
<span data-ttu-id="07542-121">접두사의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07542-121">The name of prefix.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName, ByResourceId
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07542-122">-PeeringName</span><span class="sxs-lookup"><span data-stu-id="07542-122">-PeeringName</span></span>
<span data-ttu-id="07542-123">PSPeering의 고유 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07542-123">The unique name of the PSPeering.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07542-124">-접두사</span><span class="sxs-lookup"><span data-stu-id="07542-124">-Prefix</span></span>
<span data-ttu-id="07542-125">세션 IPv4 접두사</span><span class="sxs-lookup"><span data-stu-id="07542-125">The session IPv4 prefix</span></span>

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

### <span data-ttu-id="07542-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07542-126">-ResourceGroupName</span></span>
<span data-ttu-id="07542-127">기존 리소스 그룹 이름을 만들거나 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-127">The create or use an existing resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroupAndName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="07542-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="07542-128">-ResourceId</span></span>
<span data-ttu-id="07542-129">리소스 id 문자열 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07542-129">The resource id string name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="07542-130">-확인</span><span class="sxs-lookup"><span data-stu-id="07542-130">-Confirm</span></span>
<span data-ttu-id="07542-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07542-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07542-132">-WhatIf</span></span>
<span data-ttu-id="07542-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07542-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07542-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07542-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07542-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07542-135">CommonParameters</span></span>
<span data-ttu-id="07542-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07542-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07542-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="07542-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07542-138">입력</span><span class="sxs-lookup"><span data-stu-id="07542-138">INPUTS</span></span>

### <span data-ttu-id="07542-139">PSPeeringRegisteredPrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07542-139">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

### <span data-ttu-id="07542-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07542-140">System.String</span></span>

## <span data-ttu-id="07542-141">출력</span><span class="sxs-lookup"><span data-stu-id="07542-141">OUTPUTS</span></span>

### <span data-ttu-id="07542-142">PSPeeringRegisteredPrefix (Microsoft. PowerShell.</span><span class="sxs-lookup"><span data-stu-id="07542-142">Microsoft.Azure.PowerShell.Cmdlets.Peering.Models.PSPeeringRegisteredPrefix</span></span>

## <span data-ttu-id="07542-143">상속자</span><span class="sxs-lookup"><span data-stu-id="07542-143">NOTES</span></span>

## <span data-ttu-id="07542-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07542-144">RELATED LINKS</span></span>
