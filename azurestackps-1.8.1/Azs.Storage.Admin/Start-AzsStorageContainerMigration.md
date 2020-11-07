---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: af9c5d2c5ebb547a6e09d2e4f4302ed2da470a39
ms.sourcegitcommit: fb95591c45bb5f12b98e0690938d18f2ec611897
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/15/2020
ms.locfileid: "93875063"
---
# <span data-ttu-id="87891-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="87891-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="87891-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="87891-102">SYNOPSIS</span></span>
<span data-ttu-id="87891-103">컨테이너 마이그레이션 작업을 시작 하 여 지정 된 대상 공유로 컨테이너를 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="87891-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="87891-104">구문과</span><span class="sxs-lookup"><span data-stu-id="87891-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-ContainerName] <String>
 [-ShareName] <String> [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String>
 [-AsJob] [-Force] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="87891-105">설명은</span><span class="sxs-lookup"><span data-stu-id="87891-105">DESCRIPTION</span></span>
<span data-ttu-id="87891-106">컨테이너 마이그레이션 작업을 시작 하 여 지정 된 대상 공유로 컨테이너를 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="87891-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="87891-107">예제의</span><span class="sxs-lookup"><span data-stu-id="87891-107">EXAMPLES</span></span>

### <span data-ttu-id="87891-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="87891-108">EXAMPLE 1</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -ContainerName "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="87891-109">컨테이너 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="87891-109">Starts a container migration.</span></span>

## <span data-ttu-id="87891-110">변수</span><span class="sxs-lookup"><span data-stu-id="87891-110">PARAMETERS</span></span>

### <span data-ttu-id="87891-111">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="87891-111">-StorageAccountName</span></span>
<span data-ttu-id="87891-112">컨테이너가 찾는 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87891-112">The name of storage account where the container locates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-113">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="87891-113">-ContainerName</span></span>
<span data-ttu-id="87891-114">마이그레이션할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87891-114">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-115">-ShareName</span><span class="sxs-lookup"><span data-stu-id="87891-115">-ShareName</span></span>
<span data-ttu-id="87891-116">마이그레이션에 대해 지정 된 컨테이너를 포함 하는 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87891-116">Name of the share containing the container specified for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="87891-117">-ResourceGroupName</span></span>
<span data-ttu-id="87891-118">저장소 리소스 공급자가 등록 된 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="87891-118">The resource group name in which the storage resource provider was registered under.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-119">-FarmName</span><span class="sxs-lookup"><span data-stu-id="87891-119">-FarmName</span></span>
<span data-ttu-id="87891-120">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="87891-120">Farm Id.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-121">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="87891-121">-DestinationShareUncPath</span></span>
<span data-ttu-id="87891-122">마이그레이션 대상 공유의 UNC 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="87891-122">The UNC path of the destination share for migration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 6
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="87891-123">-AsJob</span></span>
<span data-ttu-id="87891-124">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="87891-124">Run asynchronous as a job and return the job object.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-125">-Force</span><span class="sxs-lookup"><span data-stu-id="87891-125">-Force</span></span>
<span data-ttu-id="87891-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87891-126">Do not ask for confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="87891-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="87891-127">-WhatIf</span></span>
<span data-ttu-id="87891-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="87891-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="87891-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="87891-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="87891-130">-확인</span><span class="sxs-lookup"><span data-stu-id="87891-130">-Confirm</span></span>
<span data-ttu-id="87891-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="87891-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="87891-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="87891-132">CommonParameters</span></span>
<span data-ttu-id="87891-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="87891-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="87891-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="87891-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="87891-135">입력</span><span class="sxs-lookup"><span data-stu-id="87891-135">INPUTS</span></span>

## <span data-ttu-id="87891-136">출력</span><span class="sxs-lookup"><span data-stu-id="87891-136">OUTPUTS</span></span>

## <span data-ttu-id="87891-137">상속자</span><span class="sxs-lookup"><span data-stu-id="87891-137">NOTES</span></span>

## <span data-ttu-id="87891-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="87891-138">RELATED LINKS</span></span>
