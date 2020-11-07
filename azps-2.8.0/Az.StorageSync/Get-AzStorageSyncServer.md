---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncServer.md
ms.openlocfilehash: bd1665ee82dfad0bb6028252ad100e5c651d0c2d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874075"
---
# <span data-ttu-id="9a0b1-101">Get-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="9a0b1-101">Get-AzStorageSyncServer</span></span>

## <span data-ttu-id="9a0b1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a0b1-102">SYNOPSIS</span></span>
<span data-ttu-id="9a0b1-103">이 명령은 지정 된 저장소 동기화 서비스에 등록 된 모든 서버를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-103">This command lists all servers registered to a given storage sync service.</span></span>

## <span data-ttu-id="9a0b1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9a0b1-104">SYNTAX</span></span>

### <span data-ttu-id="9a0b1-105">StringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="9a0b1-105">StringParameterSet (Default)</span></span>
```
Get-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0b1-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a0b1-106">ObjectParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9a0b1-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a0b1-107">ParentStringParameterSet</span></span>
```
Get-AzStorageSyncServer [-ParentResourceId] <String> [-ServerId <Guid>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9a0b1-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9a0b1-108">DESCRIPTION</span></span>
<span data-ttu-id="9a0b1-109">이 명령은 지정 된 저장소 동기화 서비스에 등록 된 모든 서버를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-109">This command lists all servers registered to a given storage sync service.</span></span> <span data-ttu-id="9a0b1-110">또한 등록 된 각 서버의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-110">It can be used to also list the attributes of each registered server.</span></span>

## <span data-ttu-id="9a0b1-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9a0b1-111">EXAMPLES</span></span>

### <span data-ttu-id="9a0b1-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a0b1-112">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="9a0b1-113">이 명령은 특정 저장소 동기화 서비스에 등록 된 모든 서버를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-113">This command gets all servers registered to a specific storage sync service.</span></span>

## <span data-ttu-id="9a0b1-114">변수</span><span class="sxs-lookup"><span data-stu-id="9a0b1-114">PARAMETERS</span></span>

### <span data-ttu-id="9a0b1-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a0b1-115">-DefaultProfile</span></span>
<span data-ttu-id="9a0b1-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a0b1-117">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="9a0b1-117">-ParentObject</span></span>
<span data-ttu-id="9a0b1-118">일반적으로 매개 변수를 통해 전달 되는 Storages<c13> Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-118">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService
Parameter Sets: ObjectParameterSet
Aliases: StorageSyncService

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0b1-119">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="9a0b1-119">-ParentResourceId</span></span>
<span data-ttu-id="9a0b1-120">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-120">StorageSyncService Object, normally passed through the parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: StorageSyncServiceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0b1-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a0b1-121">-ResourceGroupName</span></span>
<span data-ttu-id="9a0b1-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-122">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0b1-123">-ServerId</span><span class="sxs-lookup"><span data-stu-id="9a0b1-123">-ServerId</span></span>
<span data-ttu-id="9a0b1-124">RegisteredServer의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-124">Name of the RegisteredServer.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases: RegisteredServerName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0b1-125">-Storages Cservicename</span><span class="sxs-lookup"><span data-stu-id="9a0b1-125">-StorageSyncServiceName</span></span>
<span data-ttu-id="9a0b1-126">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-126">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a0b1-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a0b1-127">CommonParameters</span></span>
<span data-ttu-id="9a0b1-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a0b1-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a0b1-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a0b1-130">입력</span><span class="sxs-lookup"><span data-stu-id="9a0b1-130">INPUTS</span></span>

### <span data-ttu-id="9a0b1-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9a0b1-131">System.String</span></span>

### <span data-ttu-id="9a0b1-132">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="9a0b1-132">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

### <span data-ttu-id="9a0b1-133">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="9a0b1-133">System.Guid</span></span>

## <span data-ttu-id="9a0b1-134">출력</span><span class="sxs-lookup"><span data-stu-id="9a0b1-134">OUTPUTS</span></span>

### <span data-ttu-id="9a0b1-135">StorageSync. PSRegisteredServer/.</span><span class="sxs-lookup"><span data-stu-id="9a0b1-135">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="9a0b1-136">상속자</span><span class="sxs-lookup"><span data-stu-id="9a0b1-136">NOTES</span></span>

## <span data-ttu-id="9a0b1-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a0b1-137">RELATED LINKS</span></span>
