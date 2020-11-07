---
external help file: Azs.Backup.Admin-help.xml
Module Name: Azs.Backup.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 364b22c834ae7476e64f972b289e20d3caa5ba80
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874263"
---
# <span data-ttu-id="1fab5-101">Get-AzsBackup</span><span class="sxs-lookup"><span data-stu-id="1fab5-101">Get-AzsBackup</span></span>

## <span data-ttu-id="1fab5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1fab5-102">SYNOPSIS</span></span>
<span data-ttu-id="1fab5-103">이름에 따라 위치에서 백업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-103">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="1fab5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1fab5-104">SYNTAX</span></span>

### <span data-ttu-id="1fab5-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="1fab5-105">List (Default)</span></span>
```
Get-AzsBackup [-Location <String>] [-ResourceGroupName <String>] [-Top <Int32>] [-Skip <Int32>]
 [<CommonParameters>]
```

### <span data-ttu-id="1fab5-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="1fab5-106">Get</span></span>
```
Get-AzsBackup -Name <String> [-Location <String>] [-ResourceGroupName <String>] [<CommonParameters>]
```

### <span data-ttu-id="1fab5-107">리소스</span><span class="sxs-lookup"><span data-stu-id="1fab5-107">ResourceId</span></span>
```
Get-AzsBackup -ResourceId <String> [<CommonParameters>]
```

### <span data-ttu-id="1fab5-108">ParentResource</span><span class="sxs-lookup"><span data-stu-id="1fab5-108">ParentResource</span></span>
```
Get-AzsBackup -ParentResource <BackupLocation> [-Top <Int32>] [-Skip <Int32>] [<CommonParameters>]
```

## <span data-ttu-id="1fab5-109">설명은</span><span class="sxs-lookup"><span data-stu-id="1fab5-109">DESCRIPTION</span></span>
<span data-ttu-id="1fab5-110">이름에 따라 위치에서 백업을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-110">Returns a backup from a location based on name.</span></span>

## <span data-ttu-id="1fab5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="1fab5-111">EXAMPLES</span></span>

### <span data-ttu-id="1fab5-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="1fab5-112">EXAMPLE 1</span></span>
```
Get-AzsBackup
```

<span data-ttu-id="1fab5-113">모든 Azure 스택 백업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-113">Get information about all Azure Stack backups.</span></span>

### <span data-ttu-id="1fab5-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="1fab5-114">EXAMPLE 2</span></span>
```
Get-AzsBackup -Name 'backupName'
```

<span data-ttu-id="1fab5-115">지정 된 Azure 스택 백업에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-115">Get information for the specified Azure Stack backup.</span></span>

## <span data-ttu-id="1fab5-116">변수</span><span class="sxs-lookup"><span data-stu-id="1fab5-116">PARAMETERS</span></span>

### <span data-ttu-id="1fab5-117">-위치</span><span class="sxs-lookup"><span data-stu-id="1fab5-117">-Location</span></span>
<span data-ttu-id="1fab5-118">위치가 백업 되었습니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-118">Location backed up.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-119">-이름</span><span class="sxs-lookup"><span data-stu-id="1fab5-119">-Name</span></span>
<span data-ttu-id="1fab5-120">백업의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-120">Name of the backup.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-121">-ParentResource</span><span class="sxs-lookup"><span data-stu-id="1fab5-121">-ParentResource</span></span>
<span data-ttu-id="1fab5-122">백업 위치를 전달 하면 해당 백업 위치에 있는 모든 백업의 목록이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-122">Passing a backup location will return the list of all backups at that backup location.</span></span>

```yaml
Type: Microsoft.AzureStack.Management.Backup.Admin.Models.BackupLocation
Parameter Sets: ParentResource
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1fab5-123">-ResourceGroupName</span></span>
<span data-ttu-id="1fab5-124">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-124">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: List, Get
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1fab5-125">-ResourceId</span></span>
<span data-ttu-id="1fab5-126">리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-126">The resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceId
Aliases: id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-127">-위쪽</span><span class="sxs-lookup"><span data-stu-id="1fab5-127">-Top</span></span>
<span data-ttu-id="1fab5-128">매개 변수 값으로 지정 된 대로 상위 N 개 항목을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-128">Return the top N items as specified by the parameter value.</span></span>
<span data-ttu-id="1fab5-129">-Skip 매개 변수 뒤에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-129">Applies after the -Skip parameter.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-130">-생략</span><span class="sxs-lookup"><span data-stu-id="1fab5-130">-Skip</span></span>
<span data-ttu-id="1fab5-131">매개 변수 값으로 지정 된 첫 N 개의 항목을 건너뜁니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-131">Skip the first N items as specified by the parameter value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: List, ParentResource
Aliases:

Required: False
Position: Named
Default value: -1
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1fab5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1fab5-132">CommonParameters</span></span>
<span data-ttu-id="1fab5-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1fab5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1fab5-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1fab5-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1fab5-135">입력</span><span class="sxs-lookup"><span data-stu-id="1fab5-135">INPUTS</span></span>

## <span data-ttu-id="1fab5-136">출력</span><span class="sxs-lookup"><span data-stu-id="1fab5-136">OUTPUTS</span></span>

### <span data-ttu-id="1fab5-137">Microsoft AzureStack. 관리. 백업 관리자. 모델</span><span class="sxs-lookup"><span data-stu-id="1fab5-137">Microsoft.AzureStack.Management.Backup.Admin.Models.Backup</span></span>

## <span data-ttu-id="1fab5-138">상속자</span><span class="sxs-lookup"><span data-stu-id="1fab5-138">NOTES</span></span>

## <span data-ttu-id="1fab5-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1fab5-139">RELATED LINKS</span></span>
