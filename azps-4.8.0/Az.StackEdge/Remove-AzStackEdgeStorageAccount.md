---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccount.md
ms.openlocfilehash: d4b815e0caa85bee26086f475f86e1757b690fbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213212"
---
# <span data-ttu-id="ee5a9-101">Remove-AzStackEdgeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="ee5a9-101">Remove-AzStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ee5a9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ee5a9-102">SYNOPSIS</span></span>
<span data-ttu-id="ee5a9-103">장치에 대 한 Edge 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-103">Removes the Edge Storage account for a device.</span></span>

## <span data-ttu-id="ee5a9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ee5a9-104">SYNTAX</span></span>

### <span data-ttu-id="ee5a9-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="ee5a9-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee5a9-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee5a9-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ee5a9-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="ee5a9-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccount [-InputObject] <PSStackEdgeStorageAccount> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ee5a9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ee5a9-108">DESCRIPTION</span></span>
<span data-ttu-id="ee5a9-109">**AzStackEdgeStorageAccount** Cmdlet은 스택 경계 장치에 대 한 연결 된 Edge 저장소 계정을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-109">The **Remove-AzStackEdgeStorageAccount** cmdlet removes an associated Edge Storage Account for a Stack Edge device.</span></span> <span data-ttu-id="ee5a9-110">Cmdlet에서 매개 변수로 제거할 Edge 저장소 계정의 이름을 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-110">You can specify the name of the Edge Storage Account to be removed as a parameter in the cmdlet.</span></span>

## <span data-ttu-id="ee5a9-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ee5a9-111">EXAMPLES</span></span>

### <span data-ttu-id="ee5a9-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="ee5a9-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccount -ResourceGroupName resourceGroupName -DeviceName deviceName -Name edgestorageaccountname
```

## <span data-ttu-id="ee5a9-113">변수</span><span class="sxs-lookup"><span data-stu-id="ee5a9-113">PARAMETERS</span></span>

### <span data-ttu-id="ee5a9-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="ee5a9-114">-AsJob</span></span>
<span data-ttu-id="ee5a9-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="ee5a9-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="ee5a9-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ee5a9-116">-DefaultProfile</span></span>
<span data-ttu-id="ee5a9-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ee5a9-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="ee5a9-118">-DeviceName</span></span>
<span data-ttu-id="ee5a9-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="ee5a9-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5a9-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ee5a9-120">-InputObject</span></span>
<span data-ttu-id="ee5a9-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="ee5a9-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: EdgeStorageAccount

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5a9-122">-이름</span><span class="sxs-lookup"><span data-stu-id="ee5a9-122">-Name</span></span>
<span data-ttu-id="ee5a9-123">자원 이름</span><span class="sxs-lookup"><span data-stu-id="ee5a9-123">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: EdgeStorageAccountName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5a9-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ee5a9-124">-PassThru</span></span>
<span data-ttu-id="ee5a9-125">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-125">returns true if successful</span></span>

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

### <span data-ttu-id="ee5a9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ee5a9-126">-ResourceGroupName</span></span>
<span data-ttu-id="ee5a9-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ee5a9-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5a9-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee5a9-128">-ResourceId</span></span>
<span data-ttu-id="ee5a9-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="ee5a9-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ee5a9-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ee5a9-130">-Confirm</span></span>
<span data-ttu-id="ee5a9-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ee5a9-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ee5a9-132">-WhatIf</span></span>
<span data-ttu-id="ee5a9-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ee5a9-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ee5a9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ee5a9-135">CommonParameters</span></span>
<span data-ttu-id="ee5a9-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ee5a9-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="ee5a9-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ee5a9-138">입력</span><span class="sxs-lookup"><span data-stu-id="ee5a9-138">INPUTS</span></span>

### <span data-ttu-id="ee5a9-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ee5a9-139">System.String</span></span>

### <span data-ttu-id="ee5a9-140">StackEdge. PSStackEdgeStorageAccount에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="ee5a9-140">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccount</span></span>

## <span data-ttu-id="ee5a9-141">출력</span><span class="sxs-lookup"><span data-stu-id="ee5a9-141">OUTPUTS</span></span>

### <span data-ttu-id="ee5a9-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ee5a9-142">System.Boolean</span></span>

## <span data-ttu-id="ee5a9-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ee5a9-143">NOTES</span></span>

## <span data-ttu-id="ee5a9-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ee5a9-144">RELATED LINKS</span></span>
