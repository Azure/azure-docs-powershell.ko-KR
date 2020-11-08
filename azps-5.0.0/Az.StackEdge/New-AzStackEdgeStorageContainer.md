---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/new-azstackedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/New-AzStackEdgeStorageContainer.md
ms.openlocfilehash: 5c0af3ed67bd7cba3408b6628de70c7064120954
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216514"
---
# <span data-ttu-id="24d57-101">New-AzStackEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24d57-101">New-AzStackEdgeStorageContainer</span></span>

## <span data-ttu-id="24d57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24d57-102">SYNOPSIS</span></span>
<span data-ttu-id="24d57-103">장치의 Edge 저장소 계정에 새 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="24d57-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24d57-104">SYNTAX</span></span>

```
New-AzStackEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24d57-105">설명은</span><span class="sxs-lookup"><span data-stu-id="24d57-105">DESCRIPTION</span></span>
<span data-ttu-id="24d57-106">**AzStackEdgeStorageContainer** Cmdlet은 스택 경계 디바이스의 edge 저장소 계정에 새 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-106">The **New-AzStackEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Stack Edge device.</span></span>

## <span data-ttu-id="24d57-107">예제의</span><span class="sxs-lookup"><span data-stu-id="24d57-107">EXAMPLES</span></span>

### <span data-ttu-id="24d57-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="24d57-108">Example 1</span></span>
```powershell
PS C:\> New-AzStackEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="24d57-109">변수</span><span class="sxs-lookup"><span data-stu-id="24d57-109">PARAMETERS</span></span>

### <span data-ttu-id="24d57-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24d57-110">-AsJob</span></span>
<span data-ttu-id="24d57-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="24d57-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="24d57-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="24d57-112">-DataFormat</span></span>
<span data-ttu-id="24d57-113">데이터 형식 설정 예: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="24d57-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="24d57-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24d57-114">-DefaultProfile</span></span>
<span data-ttu-id="24d57-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24d57-116">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="24d57-116">-DeviceName</span></span>
<span data-ttu-id="24d57-117">장치 이름</span><span class="sxs-lookup"><span data-stu-id="24d57-117">Device Name</span></span>

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

### <span data-ttu-id="24d57-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24d57-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="24d57-119">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="24d57-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="24d57-120">-이름</span><span class="sxs-lookup"><span data-stu-id="24d57-120">-Name</span></span>
<span data-ttu-id="24d57-121">자원 이름</span><span class="sxs-lookup"><span data-stu-id="24d57-121">Resource Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: EdgeContainerName

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24d57-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24d57-122">-ResourceGroupName</span></span>
<span data-ttu-id="24d57-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="24d57-123">Resource Group Name</span></span>

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

### <span data-ttu-id="24d57-124">-확인</span><span class="sxs-lookup"><span data-stu-id="24d57-124">-Confirm</span></span>
<span data-ttu-id="24d57-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24d57-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24d57-126">-WhatIf</span></span>
<span data-ttu-id="24d57-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24d57-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24d57-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24d57-129">CommonParameters</span></span>
<span data-ttu-id="24d57-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24d57-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24d57-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24d57-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24d57-132">입력</span><span class="sxs-lookup"><span data-stu-id="24d57-132">INPUTS</span></span>

### <span data-ttu-id="24d57-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24d57-133">System.String</span></span>

## <span data-ttu-id="24d57-134">출력</span><span class="sxs-lookup"><span data-stu-id="24d57-134">OUTPUTS</span></span>

### <span data-ttu-id="24d57-135">StackEdge. PSStackEdgeStorageContainer에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="24d57-135">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageContainer</span></span>

## <span data-ttu-id="24d57-136">상속자</span><span class="sxs-lookup"><span data-stu-id="24d57-136">NOTES</span></span>

## <span data-ttu-id="24d57-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24d57-137">RELATED LINKS</span></span>
