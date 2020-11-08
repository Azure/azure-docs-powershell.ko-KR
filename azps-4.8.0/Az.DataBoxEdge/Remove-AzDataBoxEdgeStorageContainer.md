---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 0e952ba845398fcd221ca7e5f4177a103b1f6155
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94215054"
---
# <span data-ttu-id="fdb7e-101">Remove-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fdb7e-101">Remove-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="fdb7e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdb7e-102">SYNOPSIS</span></span>
<span data-ttu-id="fdb7e-103">디바이스의 Edge 저장소 계정에 대 한 저장소 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-103">Removes a storage container for the Edge Storage account on a device.</span></span>

## <span data-ttu-id="fdb7e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fdb7e-104">SYNTAX</span></span>

### <span data-ttu-id="fdb7e-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="fdb7e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb7e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb7e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -ResourceId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fdb7e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="fdb7e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeStorageContainer -InputObject <PSDataBoxEdgeStorageContainer> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fdb7e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fdb7e-108">DESCRIPTION</span></span>
<span data-ttu-id="fdb7e-109">**AzDataBoxEdgeStorageContainer** Cmdlet은 데이터 상자 가장자리 디바이스의 edge 저장소 계정에 대 한 연결 된 저장소 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-109">The **Remove-AzDataBoxEdgeStorageContainer** cmdlet removes an associated storage container for the Edge Storage account on a Data Box Edge device.</span></span> <span data-ttu-id="fdb7e-110">제거할 저장소 컨테이너의 이름을 매개 변수로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-110">You can specify the name of the storage container to be removed as a parameter.</span></span>

## <span data-ttu-id="fdb7e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="fdb7e-111">EXAMPLES</span></span>

### <span data-ttu-id="fdb7e-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="fdb7e-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName deviceName -EdgeStorageAccountName edgestorageaccountname -Name container1
```

## <span data-ttu-id="fdb7e-113">변수</span><span class="sxs-lookup"><span data-stu-id="fdb7e-113">PARAMETERS</span></span>

### <span data-ttu-id="fdb7e-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fdb7e-114">-AsJob</span></span>
<span data-ttu-id="fdb7e-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fdb7e-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fdb7e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdb7e-116">-DefaultProfile</span></span>
<span data-ttu-id="fdb7e-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fdb7e-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="fdb7e-118">-DeviceName</span></span>
<span data-ttu-id="fdb7e-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="fdb7e-119">Device Name</span></span>

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

### <span data-ttu-id="fdb7e-120">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fdb7e-120">-EdgeStorageAccountName</span></span>
<span data-ttu-id="fdb7e-121">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="fdb7e-121">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb7e-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fdb7e-122">-InputObject</span></span>
<span data-ttu-id="fdb7e-123">입력 개체</span><span class="sxs-lookup"><span data-stu-id="fdb7e-123">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb7e-124">-이름</span><span class="sxs-lookup"><span data-stu-id="fdb7e-124">-Name</span></span>
<span data-ttu-id="fdb7e-125">자원 이름</span><span class="sxs-lookup"><span data-stu-id="fdb7e-125">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb7e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fdb7e-126">-PassThru</span></span>
<span data-ttu-id="fdb7e-127">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-127">returns true if successful</span></span>

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

### <span data-ttu-id="fdb7e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdb7e-128">-ResourceGroupName</span></span>
<span data-ttu-id="fdb7e-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fdb7e-129">Resource Group Name</span></span>

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

### <span data-ttu-id="fdb7e-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb7e-130">-ResourceId</span></span>
<span data-ttu-id="fdb7e-131">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="fdb7e-131">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdb7e-132">-확인</span><span class="sxs-lookup"><span data-stu-id="fdb7e-132">-Confirm</span></span>
<span data-ttu-id="fdb7e-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fdb7e-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fdb7e-134">-WhatIf</span></span>
<span data-ttu-id="fdb7e-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fdb7e-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fdb7e-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdb7e-137">CommonParameters</span></span>
<span data-ttu-id="fdb7e-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdb7e-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="fdb7e-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdb7e-140">입력</span><span class="sxs-lookup"><span data-stu-id="fdb7e-140">INPUTS</span></span>

### <span data-ttu-id="fdb7e-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fdb7e-141">System.String</span></span>

### <span data-ttu-id="fdb7e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="fdb7e-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="fdb7e-143">출력</span><span class="sxs-lookup"><span data-stu-id="fdb7e-143">OUTPUTS</span></span>

### <span data-ttu-id="fdb7e-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="fdb7e-144">System.Boolean</span></span>

## <span data-ttu-id="fdb7e-145">상속자</span><span class="sxs-lookup"><span data-stu-id="fdb7e-145">NOTES</span></span>

## <span data-ttu-id="fdb7e-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdb7e-146">RELATED LINKS</span></span>
