---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/get-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Get-AzStorageSyncService.md
ms.openlocfilehash: ec446a92c96bd92d7a4af5610f00ff76dcd50b50
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190676"
---
# <span data-ttu-id="46788-101">Get-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="46788-101">Get-AzStorageSyncService</span></span>

## <span data-ttu-id="46788-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46788-102">SYNOPSIS</span></span>
<span data-ttu-id="46788-103">이 명령은 구독/리소스 그룹의 주어진 범위 내의 모든 저장소 동기화 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="46788-103">This command lists all storage sync services within a given scope of subscription/resource group.</span></span>

## <span data-ttu-id="46788-104">구문</span><span class="sxs-lookup"><span data-stu-id="46788-104">SYNTAX</span></span>

### <span data-ttu-id="46788-105">ParentStringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="46788-105">ParentStringParameterSet (Default)</span></span>
```
Get-AzStorageSyncService [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46788-106">StringParameterSet</span><span class="sxs-lookup"><span data-stu-id="46788-106">StringParameterSet</span></span>
```
Get-AzStorageSyncService [-ResourceGroupName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46788-107">설명</span><span class="sxs-lookup"><span data-stu-id="46788-107">DESCRIPTION</span></span>
<span data-ttu-id="46788-108">이 명령은 구독/리소스 그룹의 주어진 범위 내의 모든 저장소 동기화 서비스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="46788-108">This command lists all storage sync services within a given scope of subscription/resource group.</span></span> <span data-ttu-id="46788-109">또한 각 저장소 동기화 서비스의 특성을 나열하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46788-109">It can be used to also list the attributes of each storage sync service.</span></span>

## <span data-ttu-id="46788-110">예제</span><span class="sxs-lookup"><span data-stu-id="46788-110">EXAMPLES</span></span>

### <span data-ttu-id="46788-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="46788-111">Example 1</span></span>
```powershell
PS C:\> Get-AzStorageSyncService -ResourceGroupName "myResourceGroup"
```

<span data-ttu-id="46788-112">이 명령은 주어진 리소스 그룹 내의 모든 저장소 동기화 서비스 리소스를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="46788-112">This command lists all storage sync service resources within a given resource group.</span></span> <span data-ttu-id="46788-113">또한 각 저장소 동기화 서비스의 특성을 나열하는 데 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="46788-113">It can be used to also list the attributes of each storage sync service.</span></span> <span data-ttu-id="46788-114">특정 값을 반환하도록 -StorageSyncServiceName을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="46788-114">Specify -StorageSyncServiceName to return a specific one.</span></span>

## <span data-ttu-id="46788-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="46788-115">PARAMETERS</span></span>

### <span data-ttu-id="46788-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46788-116">-DefaultProfile</span></span>
<span data-ttu-id="46788-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46788-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46788-118">-Name</span><span class="sxs-lookup"><span data-stu-id="46788-118">-Name</span></span>
<span data-ttu-id="46788-119">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46788-119">Name of the storage sync service.</span></span>

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

### <span data-ttu-id="46788-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46788-120">-ResourceGroupName</span></span>
<span data-ttu-id="46788-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46788-121">Resource Group Name.</span></span>

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

### <span data-ttu-id="46788-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46788-122">CommonParameters</span></span>
<span data-ttu-id="46788-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="46788-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46788-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="46788-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46788-125">입력</span><span class="sxs-lookup"><span data-stu-id="46788-125">INPUTS</span></span>

### <span data-ttu-id="46788-126">System.String</span><span class="sxs-lookup"><span data-stu-id="46788-126">System.String</span></span>

## <span data-ttu-id="46788-127">출력</span><span class="sxs-lookup"><span data-stu-id="46788-127">OUTPUTS</span></span>

### <span data-ttu-id="46788-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="46788-128">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="46788-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="46788-129">NOTES</span></span>

## <span data-ttu-id="46788-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46788-130">RELATED LINKS</span></span>
