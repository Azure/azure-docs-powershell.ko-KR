---
external help file: Microsoft.Azure.Commands.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/register-Azstoragesyncserver
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Register-AzStorageSyncServer.md
ms.openlocfilehash: edfeebf9781c40b44a5a06db407757a5e2f5d2a5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698484"
---
# <span data-ttu-id="b7a31-101">Register-AzStorageSyncServer</span><span class="sxs-lookup"><span data-stu-id="b7a31-101">Register-AzStorageSyncServer</span></span>

## <span data-ttu-id="b7a31-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7a31-102">SYNOPSIS</span></span>
<span data-ttu-id="b7a31-103">이 명령은 신뢰 관계를 만드는 저장소 동기화 서비스에 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-103">This command registers a server to a storage sync service which creates a trust relationship.</span></span> <span data-ttu-id="b7a31-104">그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화를 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-104">PowerShell or the Azure portal can then be used to configure sync on this server.</span></span>

## <span data-ttu-id="b7a31-105">구문과</span><span class="sxs-lookup"><span data-stu-id="b7a31-105">SYNTAX</span></span>

### <span data-ttu-id="b7a31-106">ObjectParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7a31-106">ObjectParameterSet (Default)</span></span>
```
Register-AzStorageSyncServer [-ParentObject] <PSStorageSyncService> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a31-107">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a31-107">StringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ResourceGroupName] <String> [-StorageSyncServiceName] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b7a31-108">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7a31-108">ParentStringParameterSet</span></span>
```
Register-AzStorageSyncServer [-ParentResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b7a31-109">설명은</span><span class="sxs-lookup"><span data-stu-id="b7a31-109">DESCRIPTION</span></span>
<span data-ttu-id="b7a31-110">이 명령은 Azure 파일 동기화에 대 한 최상위 리소스인 저장소 동기화 서비스에 서버를 등록 합니다. 서버와 저장소 동기화 서비스 간의 신뢰 관계를 만들어 보안 데이터 전송 및 관리 채널을 보장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-110">This command registers a server to a storage sync service, the top-level resource for Azure File Sync. A trust relationship between server and storage sync service is created that ensures secure data transfer and management channels.</span></span> <span data-ttu-id="b7a31-111">그러면 PowerShell 또는 Azure 포털을 사용 하 여이 서버에서 동기화 할 항목을 구성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-111">PowerShell or the Azure portal can then be used to configure what syncs on this server.</span></span> <span data-ttu-id="b7a31-112">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-112">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="b7a31-113">동일한 파일 집합을 동기화 하는 데 서버가 참가 해야 하는 경우 동일한 저장소 동기화 서비스에이를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-113">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>
<span data-ttu-id="b7a31-114">이 명령은 직접 실행 되거나 원격 PowerShell 세션을 통해 등록 되는 서버에서 로컬로 실행 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-114">The command must be run locally on the server that is to be registered - either executed directly or via a remote PowerShell session.</span></span> <span data-ttu-id="b7a31-115">원격 컴퓨터 개체를 수락할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-115">A remote computer object cannot be accepted.</span></span>

## <span data-ttu-id="b7a31-116">예제의</span><span class="sxs-lookup"><span data-stu-id="b7a31-116">EXAMPLES</span></span>

### <span data-ttu-id="b7a31-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7a31-117">Example 1</span></span>
```powershell
PS C:\> Register-AzStorageSyncServer -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName"
```

<span data-ttu-id="b7a31-118">이 명령은이 명령이 실행 되는 로컬 서버를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-118">This command will register the local server this command is run on.</span></span>

## <span data-ttu-id="b7a31-119">변수</span><span class="sxs-lookup"><span data-stu-id="b7a31-119">PARAMETERS</span></span>

### <span data-ttu-id="b7a31-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b7a31-120">-AsJob</span></span>
<span data-ttu-id="b7a31-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b7a31-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b7a31-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7a31-122">-DefaultProfile</span></span>
<span data-ttu-id="b7a31-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7a31-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b7a31-124">-ParentObject</span></span>
<span data-ttu-id="b7a31-125">일반적으로 매개 변수를 통해 전달 되는 Storages Cservice 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-125">StorageSyncService Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="b7a31-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b7a31-126">-ParentResourceId</span></span>
<span data-ttu-id="b7a31-127">Storages Cservice 부모 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="b7a31-127">StorageSyncService Parent Resource Id</span></span>

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

### <span data-ttu-id="b7a31-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b7a31-128">-ResourceGroupName</span></span>
<span data-ttu-id="b7a31-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="b7a31-130">-Storages<c13> Cservicename</span><span class="sxs-lookup"><span data-stu-id="b7a31-130">-StorageSyncServiceName</span></span>
<span data-ttu-id="b7a31-131">Storages Cservice의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-131">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="b7a31-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7a31-132">CommonParameters</span></span>
<span data-ttu-id="b7a31-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7a31-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7a31-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b7a31-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7a31-135">입력</span><span class="sxs-lookup"><span data-stu-id="b7a31-135">INPUTS</span></span>

### <span data-ttu-id="b7a31-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b7a31-136">System.String</span></span>

### <span data-ttu-id="b7a31-137">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="b7a31-137">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="b7a31-138">출력</span><span class="sxs-lookup"><span data-stu-id="b7a31-138">OUTPUTS</span></span>

### <span data-ttu-id="b7a31-139">StorageSync. PSRegisteredServer/.</span><span class="sxs-lookup"><span data-stu-id="b7a31-139">Microsoft.Azure.Commands.StorageSync.Models.PSRegisteredServer</span></span>

## <span data-ttu-id="b7a31-140">상속자</span><span class="sxs-lookup"><span data-stu-id="b7a31-140">NOTES</span></span>

## <span data-ttu-id="b7a31-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7a31-141">RELATED LINKS</span></span>
