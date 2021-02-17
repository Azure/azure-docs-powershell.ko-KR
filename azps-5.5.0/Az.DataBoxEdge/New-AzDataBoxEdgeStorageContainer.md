---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 3561c77e79f0ee1be82b8f180fdf1b73879dc084
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196601"
---
# <span data-ttu-id="160d5-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="160d5-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="160d5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="160d5-102">SYNOPSIS</span></span>
<span data-ttu-id="160d5-103">디바이스의 Edge Storage 계정에 새 스토리지 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="160d5-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="160d5-104">구문</span><span class="sxs-lookup"><span data-stu-id="160d5-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="160d5-105">설명</span><span class="sxs-lookup"><span data-stu-id="160d5-105">DESCRIPTION</span></span>
<span data-ttu-id="160d5-106">**New-AzDataBoxEdgeStorageContainer** cmdlet은 Data Box Edge 디바이스의 Edge Storage 계정에 새 스토리지 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="160d5-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="160d5-107">예제</span><span class="sxs-lookup"><span data-stu-id="160d5-107">EXAMPLES</span></span>

### <span data-ttu-id="160d5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="160d5-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="160d5-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="160d5-109">PARAMETERS</span></span>

### <span data-ttu-id="160d5-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="160d5-110">-AsJob</span></span>
<span data-ttu-id="160d5-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="160d5-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="160d5-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="160d5-112">-DataFormat</span></span>
<span data-ttu-id="160d5-113">데이터 형식 설정 예: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="160d5-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160d5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="160d5-114">-DefaultProfile</span></span>
<span data-ttu-id="160d5-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="160d5-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="160d5-116">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="160d5-116">-DeviceName</span></span>
<span data-ttu-id="160d5-117">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="160d5-117">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160d5-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="160d5-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="160d5-119">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="160d5-119">Provide existing EdgeStorageAccount's Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160d5-120">-Name</span><span class="sxs-lookup"><span data-stu-id="160d5-120">-Name</span></span>
<span data-ttu-id="160d5-121">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="160d5-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160d5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="160d5-122">-ResourceGroupName</span></span>
<span data-ttu-id="160d5-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="160d5-123">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="160d5-124">-Confirm</span><span class="sxs-lookup"><span data-stu-id="160d5-124">-Confirm</span></span>
<span data-ttu-id="160d5-125">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="160d5-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="160d5-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="160d5-126">-WhatIf</span></span>
<span data-ttu-id="160d5-127">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="160d5-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="160d5-128">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="160d5-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="160d5-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="160d5-129">CommonParameters</span></span>
<span data-ttu-id="160d5-130">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="160d5-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="160d5-131">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="160d5-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="160d5-132">입력</span><span class="sxs-lookup"><span data-stu-id="160d5-132">INPUTS</span></span>

### <span data-ttu-id="160d5-133">System.String</span><span class="sxs-lookup"><span data-stu-id="160d5-133">System.String</span></span>

## <span data-ttu-id="160d5-134">출력</span><span class="sxs-lookup"><span data-stu-id="160d5-134">OUTPUTS</span></span>

### <span data-ttu-id="160d5-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="160d5-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="160d5-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="160d5-136">NOTES</span></span>

## <span data-ttu-id="160d5-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="160d5-137">RELATED LINKS</span></span>
