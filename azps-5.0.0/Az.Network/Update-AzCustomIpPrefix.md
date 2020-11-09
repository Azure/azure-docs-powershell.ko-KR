---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/update-azcustomipprefix
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Update-AzCustomIpPrefix.md
ms.openlocfilehash: 65d47c57720e66ecad8267ae45f9e08eb3e4c4ca
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310745"
---
# <span data-ttu-id="0beed-101">Update-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0beed-101">Update-AzCustomIpPrefix</span></span>

## <span data-ttu-id="0beed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0beed-102">SYNOPSIS</span></span>
<span data-ttu-id="0beed-103">CustomIpPrefix를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-103">Updates a CustomIpPrefix</span></span>

## <span data-ttu-id="0beed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0beed-104">SYNTAX</span></span>

### <span data-ttu-id="0beed-105">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0beed-105">UpdateByNameParameterSet</span></span>
```
Update-AzCustomIpPrefix -Name <String> -ResourceGroupName <String> [-Commission] [-Decomission]
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0beed-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0beed-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzCustomIpPrefix -InputObject <PSCustomIpPrefix> [-Commission] [-Decomission] [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0beed-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0beed-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzCustomIpPrefix -ResourceId <String> [-Commission] [-Decomission] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0beed-108">설명은</span><span class="sxs-lookup"><span data-stu-id="0beed-108">DESCRIPTION</span></span>
<span data-ttu-id="0beed-109">**AzCustomIpPrefix** cmdlet을 사용 하면 사용자가 CustomIpPrefix를 위원회 또는 서비스 해제 하거나 리소스의 태그를 편집할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-109">The **Update-AzCustomIpPrefix** cmdlet allows the user to either commission or decommission their CustomIpPrefix, or edit the tags of the resource.</span></span>

## <span data-ttu-id="0beed-110">예제의</span><span class="sxs-lookup"><span data-stu-id="0beed-110">EXAMPLES</span></span>

### <span data-ttu-id="0beed-111">예제 1: CustomIpPrefix를 의뢰 하십시오.</span><span class="sxs-lookup"><span data-stu-id="0beed-111">Example 1 : Commission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Commission
```

<span data-ttu-id="0beed-112">위 명령으로 CustomIpPrefix의 commissioning 프로세스가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-112">The above command will start the commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="0beed-113">예제 2: CustomIpPrefix 서비스 해제</span><span class="sxs-lookup"><span data-stu-id="0beed-113">Example 2 : Decommission the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Decommission
```

<span data-ttu-id="0beed-114">위 명령으로 CustomIpPrefix의 commissioning 프로세스가 시작 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-114">The above command will start the de-commissioning process of the CustomIpPrefix.</span></span>

### <span data-ttu-id="0beed-115">예제 3: CustomIpPrefix에 대 한 업데이트 태그</span><span class="sxs-lookup"><span data-stu-id="0beed-115">Example 3 : Update tags for the CustomIpPrefix</span></span>
```powershell
PS C:\> Update-AzCustomIpPrefix -Name $prefixName -ResourceGroupName $rgName -Tag $tags
```

<span data-ttu-id="0beed-116">위 명령으로 CustomIpPrefix의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-116">The above command will update the tags for the CustomIpPrefix.</span></span>

## <span data-ttu-id="0beed-117">변수</span><span class="sxs-lookup"><span data-stu-id="0beed-117">PARAMETERS</span></span>

### <span data-ttu-id="0beed-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="0beed-118">-AsJob</span></span>
<span data-ttu-id="0beed-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0beed-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0beed-120">-수수료</span><span class="sxs-lookup"><span data-stu-id="0beed-120">-Commission</span></span>
<span data-ttu-id="0beed-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0beed-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0beed-122">-Decomission</span><span class="sxs-lookup"><span data-stu-id="0beed-122">-Decomission</span></span>
<span data-ttu-id="0beed-123">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="0beed-123">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="0beed-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0beed-124">-DefaultProfile</span></span>
<span data-ttu-id="0beed-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0beed-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="0beed-126">-InputObject</span></span>
<span data-ttu-id="0beed-127">설정할 CustomIpPrefix.</span><span class="sxs-lookup"><span data-stu-id="0beed-127">The CustomIpPrefix to set.</span></span>

```yaml
Type: PSCustomIpPrefix
Parameter Sets: SetByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0beed-128">-이름</span><span class="sxs-lookup"><span data-stu-id="0beed-128">-Name</span></span>
<span data-ttu-id="0beed-129">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-129">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0beed-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0beed-130">-ResourceGroupName</span></span>
<span data-ttu-id="0beed-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: SetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0beed-132">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0beed-132">-ResourceId</span></span>
<span data-ttu-id="0beed-133">리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-133">The resource Id.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0beed-134">태그</span><span class="sxs-lookup"><span data-stu-id="0beed-134">-Tag</span></span>
<span data-ttu-id="0beed-135">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-135">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: SetByNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Hashtable
Parameter Sets: SetByInputObjectParameterSet, SetByResourceIdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0beed-136">-확인</span><span class="sxs-lookup"><span data-stu-id="0beed-136">-Confirm</span></span>
<span data-ttu-id="0beed-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0beed-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0beed-138">-WhatIf</span></span>
<span data-ttu-id="0beed-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0beed-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0beed-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0beed-141">CommonParameters</span></span>
<span data-ttu-id="0beed-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0beed-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0beed-143">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0beed-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0beed-144">입력</span><span class="sxs-lookup"><span data-stu-id="0beed-144">INPUTS</span></span>

### <span data-ttu-id="0beed-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0beed-145">System.String</span></span>

### <span data-ttu-id="0beed-146">PSCustomIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0beed-146">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

### <span data-ttu-id="0beed-147">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="0beed-147">System.Collections.Hashtable</span></span>

## <span data-ttu-id="0beed-148">출력</span><span class="sxs-lookup"><span data-stu-id="0beed-148">OUTPUTS</span></span>

### <span data-ttu-id="0beed-149">PSCustomIpPrefix에 대 한.</span><span class="sxs-lookup"><span data-stu-id="0beed-149">Microsoft.Azure.Commands.Network.Models.PSCustomIpPrefix</span></span>

## <span data-ttu-id="0beed-150">상속자</span><span class="sxs-lookup"><span data-stu-id="0beed-150">NOTES</span></span>

## <span data-ttu-id="0beed-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0beed-151">RELATED LINKS</span></span>

[<span data-ttu-id="0beed-152">Get-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0beed-152">Get-AzCustomIpPrefix</span></span>](./Get-AzCustomIpPrefix.md)

[<span data-ttu-id="0beed-153">새로운 AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0beed-153">New-AzCustomIpPrefix</span></span>](./New-AzCustomIpPrefix.md)

[<span data-ttu-id="0beed-154">제거-AzCustomIpPrefix</span><span class="sxs-lookup"><span data-stu-id="0beed-154">Remove-AzCustomIpPrefix</span></span>](./Remove-AzCustomIpPrefix.md)