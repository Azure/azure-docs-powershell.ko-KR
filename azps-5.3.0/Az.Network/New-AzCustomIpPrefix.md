---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzCustomIpPrefix.md
ms.openlocfilehash: 08df4120e762a7837376af7413504a8fce678230
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491055"
---
# <span data-ttu-id="3cb52-101">New-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3cb52-101">New-AzCustomIpPrefix</span></span>

## <span data-ttu-id="3cb52-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cb52-102">SYNOPSIS</span></span>
<span data-ttu-id="3cb52-103">CustomIpPrefix 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-103">Creates a CustomIpPrefix resource</span></span>

## <span data-ttu-id="3cb52-104">구문</span><span class="sxs-lookup"><span data-stu-id="3cb52-104">SYNTAX</span></span>

```
New-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> -Location <String> -Cidr <String>
 [-Zone <String[]>] [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3cb52-105">설명</span><span class="sxs-lookup"><span data-stu-id="3cb52-105">DESCRIPTION</span></span>
<span data-ttu-id="3cb52-106">**New-AzCustomIpPrefix** cmdlet은 CustomIpPrefix 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-106">The **New-AzCustomIpPrefix** cmdlet creates a CustomIpPrefix resource.</span></span>

## <span data-ttu-id="3cb52-107">예제</span><span class="sxs-lookup"><span data-stu-id="3cb52-107">EXAMPLES</span></span>

### <span data-ttu-id="3cb52-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cb52-108">Example 1</span></span>
```powershell
PS C:\> $myCustomIpPrefix = New-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Cidr 40.40.40.0/24 -Location westus
```

<span data-ttu-id="3cb52-109">이 명령은 westus에서 $prefixName 40.40.40.0/24의 cidr를 사용하여 리소스 $rgName 이름의 새 CustomIpPrefix 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-109">This command creates a new CustomIpPrefix resource with name $prefixName in resource group $rgName with a cidr of 40.40.40.0/24 in westus</span></span>

## <span data-ttu-id="3cb52-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3cb52-110">PARAMETERS</span></span>

### <span data-ttu-id="3cb52-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3cb52-111">-AsJob</span></span>
<span data-ttu-id="3cb52-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3cb52-112">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-113">-Cidr</span><span class="sxs-lookup"><span data-stu-id="3cb52-113">-Cidr</span></span>
<span data-ttu-id="3cb52-114">CustomIpPrefix CIDR입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-114">The CustomIpPrefix CIDR.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cb52-115">-DefaultProfile</span></span>
<span data-ttu-id="3cb52-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-117">-Location</span><span class="sxs-lookup"><span data-stu-id="3cb52-117">-Location</span></span>
<span data-ttu-id="3cb52-118">CustomIpPrefix 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-118">The CustomIpPrefix location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-119">-Name</span><span class="sxs-lookup"><span data-stu-id="3cb52-119">-Name</span></span>
<span data-ttu-id="3cb52-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-120">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3cb52-121">-ResourceGroupName</span></span>
<span data-ttu-id="3cb52-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-123">-Tag</span><span class="sxs-lookup"><span data-stu-id="3cb52-123">-Tag</span></span>
<span data-ttu-id="3cb52-124">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-124">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-125">-Zone</span><span class="sxs-lookup"><span data-stu-id="3cb52-125">-Zone</span></span>
<span data-ttu-id="3cb52-126">리소스에 할당된 IP를 표시하는 가용성 영역 목록이 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-126">A list of availability zones denoting the IP allocated for the resource needs to come from.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="3cb52-127">-Confirm</span></span>
<span data-ttu-id="3cb52-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-128">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3cb52-129">-WhatIf</span></span>
<span data-ttu-id="3cb52-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="3cb52-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3cb52-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-131">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3cb52-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cb52-132">CommonParameters</span></span>
<span data-ttu-id="3cb52-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3cb52-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cb52-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="3cb52-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cb52-135">입력</span><span class="sxs-lookup"><span data-stu-id="3cb52-135">INPUTS</span></span>

### <span data-ttu-id="3cb52-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3cb52-136">System.String</span></span>

### <span data-ttu-id="3cb52-137">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3cb52-137">System.String[]</span></span>

### <span data-ttu-id="3cb52-138">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3cb52-138">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3cb52-139">출력</span><span class="sxs-lookup"><span data-stu-id="3cb52-139">OUTPUTS</span></span>

### <span data-ttu-id="3cb52-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3cb52-140">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="3cb52-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3cb52-141">NOTES</span></span>

## <span data-ttu-id="3cb52-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cb52-142">RELATED LINKS</span></span>

[<span data-ttu-id="3cb52-143">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3cb52-143">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="3cb52-144">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3cb52-144">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)

[<span data-ttu-id="3cb52-145">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="3cb52-145">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)