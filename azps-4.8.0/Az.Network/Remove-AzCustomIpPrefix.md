---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzCustomIpPrefix.md
ms.openlocfilehash: bcb250c8967c10e5b200e62d843e99eab374d81d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214348"
---
# <span data-ttu-id="0d827-101">Remove-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d827-101">Remove-AzCustomIpPrefix</span></span>

## <span data-ttu-id="0d827-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0d827-102">SYNOPSIS</span></span>
<span data-ttu-id="0d827-103">CustomIpPrefix 제거</span><span class="sxs-lookup"><span data-stu-id="0d827-103">Removes a CustomIpPrefix</span></span>

## <span data-ttu-id="0d827-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0d827-104">SYNTAX</span></span>

### <span data-ttu-id="0d827-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0d827-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d827-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d827-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzCustomIpPrefix -ResourceId <String> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0d827-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0d827-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Force] [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0d827-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0d827-108">DESCRIPTION</span></span>
<span data-ttu-id="0d827-109">**AzCustomIpPrefix** Cmdlet은 CustomIpPrefix를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-109">The **Remove-AzCustomIpPrefix** cmdlet removes a CustomIpPrefix.</span></span>

## <span data-ttu-id="0d827-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0d827-110">EXAMPLES</span></span>

### <span data-ttu-id="0d827-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="0d827-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName
```

<span data-ttu-id="0d827-112">리소스 그룹에서 이름이 $prefixName 인 CustomIpPrefix을 제거 $rgName</span><span class="sxs-lookup"><span data-stu-id="0d827-112">Removes the CustomIpPrefix with Name $prefixName from resource group $rgName</span></span>

## <span data-ttu-id="0d827-113">변수</span><span class="sxs-lookup"><span data-stu-id="0d827-113">PARAMETERS</span></span>

### <span data-ttu-id="0d827-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0d827-114">-AsJob</span></span>
<span data-ttu-id="0d827-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0d827-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0d827-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0d827-116">-DefaultProfile</span></span>
<span data-ttu-id="0d827-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0d827-118">-Force</span><span class="sxs-lookup"><span data-stu-id="0d827-118">-Force</span></span>
<span data-ttu-id="0d827-119">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-119">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="0d827-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0d827-120">-InputObject</span></span>
<span data-ttu-id="0d827-121">CustomIpPrefix 개체</span><span class="sxs-lookup"><span data-stu-id="0d827-121">A customIpPrefix object.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0d827-122">-이름</span><span class="sxs-lookup"><span data-stu-id="0d827-122">-Name</span></span>
<span data-ttu-id="0d827-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-123">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d827-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0d827-124">-PassThru</span></span>
<span data-ttu-id="0d827-125">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-125">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0d827-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-126">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="0d827-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0d827-127">-ResourceGroupName</span></span>
<span data-ttu-id="0d827-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-128">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d827-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0d827-129">-ResourceId</span></span>
<span data-ttu-id="0d827-130">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-130">The resource id.</span></span>

```yaml
Type: String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0d827-131">-확인</span><span class="sxs-lookup"><span data-stu-id="0d827-131">-Confirm</span></span>
<span data-ttu-id="0d827-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0d827-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0d827-133">-WhatIf</span></span>
<span data-ttu-id="0d827-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0d827-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0d827-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0d827-136">CommonParameters</span></span>
<span data-ttu-id="0d827-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0d827-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0d827-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0d827-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0d827-139">입력</span><span class="sxs-lookup"><span data-stu-id="0d827-139">INPUTS</span></span>

### <span data-ttu-id="0d827-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0d827-140">System.String</span></span>

### <span data-ttu-id="0d827-141">PSCustomIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0d827-141">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="0d827-142">출력</span><span class="sxs-lookup"><span data-stu-id="0d827-142">OUTPUTS</span></span>

### <span data-ttu-id="0d827-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="0d827-143">System.Boolean</span></span>

## <span data-ttu-id="0d827-144">상속자</span><span class="sxs-lookup"><span data-stu-id="0d827-144">NOTES</span></span>

## <span data-ttu-id="0d827-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0d827-145">RELATED LINKS</span></span>

[<span data-ttu-id="0d827-146">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d827-146">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="0d827-147">새로운 AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d827-147">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="0d827-148">업데이트-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0d827-148">Update-AzCustomIpPrefix</span></span>](./Update-AzCustomIpPrefix.md)