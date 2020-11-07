---
external help file: Azs.Storage.Admin-help.xml
Module Name: Azs.Storage.Admin
online version: ''
schema: 2.0.0
ms.openlocfilehash: 54016a200b4304c7e37777202a8450fc9ad10e1e
ms.sourcegitcommit: a6f2fc500242de6248224278d743fd09aac2fafd
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2020
ms.locfileid: "93874721"
---
# <span data-ttu-id="5352b-101">Start-AzsStorageContainerMigration</span><span class="sxs-lookup"><span data-stu-id="5352b-101">Start-AzsStorageContainerMigration</span></span>

## <span data-ttu-id="5352b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5352b-102">SYNOPSIS</span></span>
<span data-ttu-id="5352b-103">컨테이너 마이그레이션 작업을 시작 하 여 지정 된 대상 공유로 컨테이너를 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-103">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="5352b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5352b-104">SYNTAX</span></span>

```
Start-AzsStorageContainerMigration [-StorageAccountName] <String> [-Name] <String> [-ShareName] <String>
 [[-ResourceGroupName] <String>] [-FarmName] <String> [-DestinationShareUncPath] <String> [-AsJob] [-Force]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5352b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5352b-105">DESCRIPTION</span></span>
<span data-ttu-id="5352b-106">컨테이너 마이그레이션 작업을 시작 하 여 지정 된 대상 공유로 컨테이너를 마이그레이션합니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-106">Starts a container migration job to migrate containers to the specified destination share.</span></span>

## <span data-ttu-id="5352b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5352b-107">EXAMPLES</span></span>

### <span data-ttu-id="5352b-108">--------------------------예제 1--------------------------</span><span class="sxs-lookup"><span data-stu-id="5352b-108">-------------------------- EXAMPLE 1 --------------------------</span></span>
```
Start-AzsStorageContainerMigration -StorageAccountName "accountTest" -Name "containerTest" -ShareName "shareTest" -FarmName "10e8d576-d73c-454c-a40a-aee31a77a5f0" -DestinationShareUncPath "\\***.***.***.***\C$\Test"
```

<span data-ttu-id="5352b-109">컨테이너 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-109">Starts a container migration.</span></span>

## <span data-ttu-id="5352b-110">변수</span><span class="sxs-lookup"><span data-stu-id="5352b-110">PARAMETERS</span></span>

### <span data-ttu-id="5352b-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5352b-111">-AsJob</span></span>
<span data-ttu-id="5352b-112">비동기를 작업으로 실행 하 고 작업 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-112">Run asynchronous as a job and return the job object.</span></span>

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

### <span data-ttu-id="5352b-113">-DestinationShareUncPath</span><span class="sxs-lookup"><span data-stu-id="5352b-113">-DestinationShareUncPath</span></span>
<span data-ttu-id="5352b-114">마이그레이션 대상 공유의 UNC 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-114">The UNC path of the destination share for migration.</span></span>

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

### <span data-ttu-id="5352b-115">-FarmName</span><span class="sxs-lookup"><span data-stu-id="5352b-115">-FarmName</span></span>
<span data-ttu-id="5352b-116">팜 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-116">Farm Id.</span></span>

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

### <span data-ttu-id="5352b-117">-Force</span><span class="sxs-lookup"><span data-stu-id="5352b-117">-Force</span></span>
<span data-ttu-id="5352b-118">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-118">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="5352b-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5352b-119">-Name</span></span>
<span data-ttu-id="5352b-120">마이그레이션할 컨테이너의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-120">The name of the container to be migrated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5352b-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5352b-121">-ResourceGroupName</span></span>
<span data-ttu-id="5352b-122">저장소 리소스 공급자가 등록 된 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-122">The resource group name in which the storage resource provider was registered under.</span></span>

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

### <span data-ttu-id="5352b-123">-ShareName</span><span class="sxs-lookup"><span data-stu-id="5352b-123">-ShareName</span></span>
<span data-ttu-id="5352b-124">마이그레이션에 대해 지정 된 컨테이너를 포함 하는 공유의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-124">Name of the share containing the container specified for migration.</span></span>

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

### <span data-ttu-id="5352b-125">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="5352b-125">-StorageAccountName</span></span>
<span data-ttu-id="5352b-126">컨테이너가 찾는 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-126">The name of storage account where the container locates.</span></span>

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

### <span data-ttu-id="5352b-127">-확인</span><span class="sxs-lookup"><span data-stu-id="5352b-127">-Confirm</span></span>
<span data-ttu-id="5352b-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5352b-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5352b-129">-WhatIf</span></span>
<span data-ttu-id="5352b-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5352b-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5352b-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5352b-132">CommonParameters</span></span>
<span data-ttu-id="5352b-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5352b-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5352b-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5352b-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5352b-135">입력</span><span class="sxs-lookup"><span data-stu-id="5352b-135">INPUTS</span></span>

## <span data-ttu-id="5352b-136">출력</span><span class="sxs-lookup"><span data-stu-id="5352b-136">OUTPUTS</span></span>

## <span data-ttu-id="5352b-137">상속자</span><span class="sxs-lookup"><span data-stu-id="5352b-137">NOTES</span></span>

## <span data-ttu-id="5352b-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5352b-138">RELATED LINKS</span></span>

