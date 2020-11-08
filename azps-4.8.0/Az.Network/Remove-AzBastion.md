---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzBastion.md
ms.openlocfilehash: 8030b0efbac800add6914d4da67821e35168f2de
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214102"
---
# <span data-ttu-id="2c731-101">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2c731-101">Remove-AzBastion</span></span>

## <span data-ttu-id="2c731-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c731-102">SYNOPSIS</span></span>
<span data-ttu-id="2c731-103">방호 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-103">Removes a bastion resource.</span></span>

## <span data-ttu-id="2c731-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2c731-104">SYNTAX</span></span>

### <span data-ttu-id="2c731-105">ByResourceGroupName (기본값)</span><span class="sxs-lookup"><span data-stu-id="2c731-105">ByResourceGroupName (Default)</span></span>
```
Remove-AzBastion -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c731-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="2c731-106">ByInputObject</span></span>
```
Remove-AzBastion -InputObject <PSBastion> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c731-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="2c731-107">ByResourceId</span></span>
```
Remove-AzBastion -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c731-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2c731-108">DESCRIPTION</span></span>
<span data-ttu-id="2c731-109">방호 리소스를 제거 합니다. Example1는 해당 ResourceGroupName 및 Context.resourcename을 사용 하 여 방호를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-109">Removes a bastion resource.Example1 deletes the bastion using its ResourceGroupName and ResourceName.</span></span> <span data-ttu-id="2c731-110">Example2는 파이프라인으로 해당 개체를 사용 하 여 방호를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-110">Example2 deletes the bastion using its object with pipeline.</span></span> <span data-ttu-id="2c731-111">Example3는 해당 개체를 사용 하 여 방호를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-111">Example3 deletes the bastion using its object.</span></span>

## <span data-ttu-id="2c731-112">예제의</span><span class="sxs-lookup"><span data-stu-id="2c731-112">EXAMPLES</span></span>

### <span data-ttu-id="2c731-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="2c731-113">Example 1</span></span>
```powershell
Remove-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion2"
```

### <span data-ttu-id="2c731-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="2c731-114">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion" | Remove-AzBastion
 ```

### <span data-ttu-id="2c731-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="2c731-115">Example 3</span></span>
```powershell
$bastion = Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"
Remove-AzBastion -InputObject $bastion
 ```

## <span data-ttu-id="2c731-116">변수</span><span class="sxs-lookup"><span data-stu-id="2c731-116">PARAMETERS</span></span>

### <span data-ttu-id="2c731-117">-확인</span><span class="sxs-lookup"><span data-stu-id="2c731-117">-Confirm</span></span>
<span data-ttu-id="2c731-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c731-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c731-119">-DefaultProfile</span></span>
<span data-ttu-id="2c731-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c731-121">-Force</span><span class="sxs-lookup"><span data-stu-id="2c731-121">-Force</span></span>
<span data-ttu-id="2c731-122">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-122">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="2c731-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c731-123">-InputObject</span></span>
<span data-ttu-id="2c731-124">삭제할 방호 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-124">The Bastion object to be deleted.</span></span>

```yaml
Type: PSBastion
Parameter Sets: ByInputObject
Aliases: Bastion, BastionObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2c731-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2c731-125">-Name</span></span>
<span data-ttu-id="2c731-126">삭제할 방호 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-126">The bastion resource name to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c731-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2c731-127">-PassThru</span></span>
<span data-ttu-id="2c731-128">이 작업이 수행 되는 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-128">Returns an object representing the item on which this operation is being performed.</span></span>

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

### <span data-ttu-id="2c731-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2c731-129">-ResourceGroupName</span></span>
<span data-ttu-id="2c731-130">방호가 있는 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-130">The resource group name where bastion exists.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2c731-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2c731-131">-ResourceId</span></span>
<span data-ttu-id="2c731-132">삭제할 방호의 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-132">The Azure resource ID for the Bastion to be deleted.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases: BastionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2c731-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c731-133">-WhatIf</span></span>
<span data-ttu-id="2c731-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c731-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c731-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c731-136">CommonParameters</span></span>
<span data-ttu-id="2c731-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2c731-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c731-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2c731-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c731-139">입력</span><span class="sxs-lookup"><span data-stu-id="2c731-139">INPUTS</span></span>

### <span data-ttu-id="2c731-140">Microsoft. 네트워크 모델. PSBastion</span><span class="sxs-lookup"><span data-stu-id="2c731-140">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="2c731-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="2c731-141">System.String</span></span>

## <span data-ttu-id="2c731-142">출력</span><span class="sxs-lookup"><span data-stu-id="2c731-142">OUTPUTS</span></span>

### <span data-ttu-id="2c731-143">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="2c731-143">System.Boolean</span></span>

## <span data-ttu-id="2c731-144">상속자</span><span class="sxs-lookup"><span data-stu-id="2c731-144">NOTES</span></span>

## <span data-ttu-id="2c731-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c731-145">RELATED LINKS</span></span>
[<span data-ttu-id="2c731-146">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="2c731-146">Get-AzBastion</span></span>](./Get-AzBastion.md)

[<span data-ttu-id="2c731-147">새로운 AzBastion</span><span class="sxs-lookup"><span data-stu-id="2c731-147">New-AzBastion</span></span>](./New-AzBastion.md)