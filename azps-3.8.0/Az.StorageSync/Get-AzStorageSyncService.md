---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878018"
---
# <span data-ttu-id="00e33-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="00e33-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="00e33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="00e33-102">SYNOPSIS</span></span>
<span data-ttu-id="00e33-103">이 명령은 구독/리소스 그룹의 지정 된 범위 내에 있는 모든 저장소 동기화 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="00e33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="00e33-104">SYNTAX</span></span>

### <span data-ttu-id="00e33-105">ParentStringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="00e33-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="00e33-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="00e33-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="00e33-107">설명은</span><span class="sxs-lookup"><span data-stu-id="00e33-107">DESCRIPTION</span></span>
<span data-ttu-id="00e33-108">이 명령은 구독/리소스 그룹의 지정 된 범위 내에 있는 모든 저장소 동기화 서비스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="00e33-109">또한 각 저장소 동기화 서비스의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="00e33-110">예제의</span><span class="sxs-lookup"><span data-stu-id="00e33-110">EXAMPLES</span></span>

### <span data-ttu-id="00e33-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="00e33-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="00e33-112">이 명령은 지정 된 리소스 그룹 내의 모든 저장소 동기화 서비스 리소스를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="00e33-113">또한 각 저장소 동기화 서비스의 특성을 나열 하는 데 사용 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="00e33-114">특정 항목을 반환 하려면-Storages<c13> Cservicename을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="00e33-115">변수</span><span class="sxs-lookup"><span data-stu-id="00e33-115">PARAMETERS</span></span>

### <span data-ttu-id="00e33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="00e33-116">-DefaultProfile</span></span>
<span data-ttu-id="00e33-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="00e33-118">-이름</span><span class="sxs-lookup"><span data-stu-id="00e33-118">-Name</span></span>
<span data-ttu-id="00e33-119">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-119">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: StorageSyncServiceName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="00e33-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="00e33-120">-ResourceGroupName</span></span>
<span data-ttu-id="00e33-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-121">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="00e33-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="00e33-122">CommonParameters</span></span>
<span data-ttu-id="00e33-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="00e33-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="00e33-124">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="00e33-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="00e33-125">입력</span><span class="sxs-lookup"><span data-stu-id="00e33-125">INPUTS</span></span>

### <span data-ttu-id="00e33-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="00e33-126">System.String</span></span>

## <span data-ttu-id="00e33-127">출력</span><span class="sxs-lookup"><span data-stu-id="00e33-127">OUTPUTS</span></span>

### <span data-ttu-id="00e33-128">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="00e33-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="00e33-129">상속자</span><span class="sxs-lookup"><span data-stu-id="00e33-129">NOTES</span></span>

## <span data-ttu-id="00e33-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="00e33-130">RELATED LINKS</span></span>
