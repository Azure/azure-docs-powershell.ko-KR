---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/new-azdataboxedgestoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/New-AzDataBoxEdgeStorageContainer.md
ms.openlocfilehash: 8d8057953c6a5fcccd5ea561eda36c623b3e5c85
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876800"
---
# <span data-ttu-id="1e9fa-101">New-AzDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1e9fa-101">New-AzDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="1e9fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e9fa-102">SYNOPSIS</span></span>
<span data-ttu-id="1e9fa-103">장치의 Edge 저장소 계정에 새 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-103">Creates a new storage container in the Edge Storage account on the device.</span></span>

## <span data-ttu-id="1e9fa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e9fa-104">SYNTAX</span></span>

```
New-AzDataBoxEdgeStorageContainer [-ResourceGroupName] <String> [-DeviceName] <String>
 [-EdgeStorageAccountName] <String> [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-DataFormat <String>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1e9fa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e9fa-105">DESCRIPTION</span></span>
<span data-ttu-id="1e9fa-106">**AzDataBoxEdgeStorageContainer** Cmdlet은 데이터 상자 가장자리 장치의 edge 저장소 계정에 새 저장소 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-106">The **New-AzDataBoxEdgeStorageContainer** cmdlet creates a new storage container in the Edge Storage account on a Data Box Edge device.</span></span>

## <span data-ttu-id="1e9fa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e9fa-107">EXAMPLES</span></span>

### <span data-ttu-id="1e9fa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1e9fa-108">Example 1</span></span>
```powershell
PS C:\> New-AzDataBoxEdgeStorageContainer -ResourceGroupName resourceGroupName -DeviceName db-edge -EdgeStorageAccountName edgestorageaccount1 -Name edgecontainer1 -DataFormat BlockBlob
Name       DataFormat EdgeStorageAccountName DeviceName ResourceGroupName
----       ---------- ---------------------- ---------- -----------------
container1 BlockBlob  edgestorageaccount1    db-edge    resourceGroupName
```

## <span data-ttu-id="1e9fa-109">변수</span><span class="sxs-lookup"><span data-stu-id="1e9fa-109">PARAMETERS</span></span>

### <span data-ttu-id="1e9fa-110">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1e9fa-110">-AsJob</span></span>
<span data-ttu-id="1e9fa-111">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1e9fa-111">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1e9fa-112">-DataFormat</span><span class="sxs-lookup"><span data-stu-id="1e9fa-112">-DataFormat</span></span>
<span data-ttu-id="1e9fa-113">데이터 형식 설정 예: PageBlob, BlobBlob</span><span class="sxs-lookup"><span data-stu-id="1e9fa-113">Set Data Format ex: PageBlob, BlobBlob</span></span>

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

### <span data-ttu-id="1e9fa-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e9fa-114">-DefaultProfile</span></span>
<span data-ttu-id="1e9fa-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e9fa-116">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="1e9fa-116">-DeviceName</span></span>
<span data-ttu-id="1e9fa-117">장치 이름</span><span class="sxs-lookup"><span data-stu-id="1e9fa-117">Device Name</span></span>

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

### <span data-ttu-id="1e9fa-118">-EdgeStorageAccountName</span><span class="sxs-lookup"><span data-stu-id="1e9fa-118">-EdgeStorageAccountName</span></span>
<span data-ttu-id="1e9fa-119">기존 EdgeStorageAccount의 이름 제공</span><span class="sxs-lookup"><span data-stu-id="1e9fa-119">Provide existing EdgeStorageAccount's Name</span></span>

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

### <span data-ttu-id="1e9fa-120">-이름</span><span class="sxs-lookup"><span data-stu-id="1e9fa-120">-Name</span></span>
<span data-ttu-id="1e9fa-121">자원 이름</span><span class="sxs-lookup"><span data-stu-id="1e9fa-121">Resource Name</span></span>

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

### <span data-ttu-id="1e9fa-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1e9fa-122">-ResourceGroupName</span></span>
<span data-ttu-id="1e9fa-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1e9fa-123">Resource Group Name</span></span>

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

### <span data-ttu-id="1e9fa-124">-확인</span><span class="sxs-lookup"><span data-stu-id="1e9fa-124">-Confirm</span></span>
<span data-ttu-id="1e9fa-125">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1e9fa-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1e9fa-126">-WhatIf</span></span>
<span data-ttu-id="1e9fa-127">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-127">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1e9fa-128">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1e9fa-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e9fa-129">CommonParameters</span></span>
<span data-ttu-id="1e9fa-130">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e9fa-131">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1e9fa-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e9fa-132">입력</span><span class="sxs-lookup"><span data-stu-id="1e9fa-132">INPUTS</span></span>

### <span data-ttu-id="1e9fa-133">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1e9fa-133">System.String</span></span>

## <span data-ttu-id="1e9fa-134">출력</span><span class="sxs-lookup"><span data-stu-id="1e9fa-134">OUTPUTS</span></span>

### <span data-ttu-id="1e9fa-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span><span class="sxs-lookup"><span data-stu-id="1e9fa-135">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageContainer</span></span>

## <span data-ttu-id="1e9fa-136">상속자</span><span class="sxs-lookup"><span data-stu-id="1e9fa-136">NOTES</span></span>

## <span data-ttu-id="1e9fa-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e9fa-137">RELATED LINKS</span></span>
