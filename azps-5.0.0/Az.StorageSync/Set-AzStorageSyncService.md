---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/set-Azstoragesyncservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/Set-AzStorageSyncService.md
ms.openlocfilehash: 2e22912df9a567ac836f22c8ac82d0a70610f2f3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217984"
---
# <span data-ttu-id="98c13-101">Set-AzStorageSyncService</span><span class="sxs-lookup"><span data-stu-id="98c13-101">Set-AzStorageSyncService</span></span>

## <span data-ttu-id="98c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98c13-102">SYNOPSIS</span></span>
<span data-ttu-id="98c13-103">이 명령은 리소스 그룹에 저장소 동기화 서비스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-103">This command sets storage sync service in a resource group.</span></span>

## <span data-ttu-id="98c13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="98c13-104">SYNTAX</span></span>

```
Set-AzStorageSyncService [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="98c13-105">설명은</span><span class="sxs-lookup"><span data-stu-id="98c13-105">DESCRIPTION</span></span>
<span data-ttu-id="98c13-106">저장소 동기화 서비스는 Azure 파일 동기화를 위한 최상위 수준 리소스입니다. 이 명령은 리소스 그룹에 저장소 동기화 서비스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-106">A storage sync service is the top level resource for Azure File Sync. This command sets storage sync service in a resource group.</span></span> <span data-ttu-id="98c13-107">조직의 개별 서버 그룹을 구분 하는 데 필요한 만큼의 저장소 동기화 서비스를 만드는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-107">We recommend to create as few storage sync services as absolutely necessary to differentiate distinct groups of servers in your organization.</span></span> <span data-ttu-id="98c13-108">저장소 동기화 서비스에는 동기화 그룹이 포함 되며, 서버를 등록할 대상으로도 작동 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-108">A storage sync service contains sync groups and also works as a target to register your servers to.</span></span> <span data-ttu-id="98c13-109">서버는 단일 저장소 동기화 서비스에만 등록할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-109">A server can only be registered to a single storage sync service.</span></span> <span data-ttu-id="98c13-110">동일한 파일 집합을 동기화 하는 데 서버가 참가 해야 하는 경우 동일한 저장소 동기화 서비스에이를 등록 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-110">If servers ever need to participate in syncing the same set of files, register them to the same storage sync service.</span></span>

## <span data-ttu-id="98c13-111">예제의</span><span class="sxs-lookup"><span data-stu-id="98c13-111">EXAMPLES</span></span>

### <span data-ttu-id="98c13-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="98c13-112">Example 1</span></span>
```powershell
PS C:\> Set-AzStorageSyncService -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -IncomingTrafficPolicy "AllowAllTraffic"
```

<span data-ttu-id="98c13-113">이 명령은 저장소 동기화 서비스를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-113">This command will set a storage sync service.</span></span>

## <span data-ttu-id="98c13-114">변수</span><span class="sxs-lookup"><span data-stu-id="98c13-114">PARAMETERS</span></span>

### <span data-ttu-id="98c13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98c13-115">-DefaultProfile</span></span>
<span data-ttu-id="98c13-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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
### <span data-ttu-id="98c13-117">-이름</span><span class="sxs-lookup"><span data-stu-id="98c13-117">-Name</span></span>
<span data-ttu-id="98c13-118">저장소 동기화 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-118">Name of the storage sync service.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageSyncServiceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98c13-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="98c13-119">-ResourceGroupName</span></span>
<span data-ttu-id="98c13-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="98c13-121">-IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="98c13-121">-IncomingTrafficPolicy</span></span>
<span data-ttu-id="98c13-122">저장소 동기화 서비스 IncomingTrafficPolicy</span><span class="sxs-lookup"><span data-stu-id="98c13-122">Storage Sync Service IncomingTrafficPolicy</span></span>

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

### <span data-ttu-id="98c13-123">태그</span><span class="sxs-lookup"><span data-stu-id="98c13-123">-Tag</span></span>
<span data-ttu-id="98c13-124">저장소 동기화 서비스 태그.</span><span class="sxs-lookup"><span data-stu-id="98c13-124">Storage Sync Service Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="98c13-125">-확인</span><span class="sxs-lookup"><span data-stu-id="98c13-125">-Confirm</span></span>
<span data-ttu-id="98c13-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="98c13-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="98c13-127">-WhatIf</span></span>
<span data-ttu-id="98c13-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-128">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="98c13-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="98c13-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98c13-130">CommonParameters</span></span>
<span data-ttu-id="98c13-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="98c13-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98c13-132">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98c13-132">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98c13-133">입력</span><span class="sxs-lookup"><span data-stu-id="98c13-133">INPUTS</span></span>

### <span data-ttu-id="98c13-134">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="98c13-134">System.String</span></span>

## <span data-ttu-id="98c13-135">출력</span><span class="sxs-lookup"><span data-stu-id="98c13-135">OUTPUTS</span></span>

### <span data-ttu-id="98c13-136">StorageSync. Psstorages Cservice</span><span class="sxs-lookup"><span data-stu-id="98c13-136">Microsoft.Azure.Commands.StorageSync.Models.PSStorageSyncService</span></span>

## <span data-ttu-id="98c13-137">상속자</span><span class="sxs-lookup"><span data-stu-id="98c13-137">NOTES</span></span>

## <span data-ttu-id="98c13-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="98c13-138">RELATED LINKS</span></span>
