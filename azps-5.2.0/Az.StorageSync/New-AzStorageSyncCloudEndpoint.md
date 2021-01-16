---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/en-us/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: 95b30bda3d824fccc5bb40e442697b81b6396d56
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366682"
---
# <span data-ttu-id="b93a7-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b93a7-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="b93a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b93a7-102">SYNOPSIS</span></span>
<span data-ttu-id="b93a7-103">이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="b93a7-104">구문</span><span class="sxs-lookup"><span data-stu-id="b93a7-104">SYNTAX</span></span>

### <span data-ttu-id="b93a7-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b93a7-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b93a7-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93a7-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b93a7-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b93a7-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b93a7-108">설명</span><span class="sxs-lookup"><span data-stu-id="b93a7-108">DESCRIPTION</span></span>
<span data-ttu-id="b93a7-109">이 명령은 Azure 파일 동기화 클라우드 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="b93a7-110">클라우드 엔드포인트는 기존 Azure 파일 공유에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="b93a7-111">파일 공유를 나타내고 클라우드 엔드포인트가 만들어진 동기화 그룹의 모든 파일 부분을 동기화하는 참여를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="b93a7-112">예제</span><span class="sxs-lookup"><span data-stu-id="b93a7-112">EXAMPLES</span></span>

### <span data-ttu-id="b93a7-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="b93a7-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="b93a7-114">클라우드 엔드포인트는 동기화 그룹의 정수 멤버입니다. 이 예제는 "mySyncGroupName"이라는 기존 동기화 그룹 내에서 만드는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="b93a7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b93a7-115">PARAMETERS</span></span>

### <span data-ttu-id="b93a7-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b93a7-116">-AsJob</span></span>
<span data-ttu-id="b93a7-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b93a7-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b93a7-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="b93a7-118">-AzureFileShareName</span></span>
<span data-ttu-id="b93a7-119">Storage 계정 공유 이름(Azure 파일 공유 이름)</span><span class="sxs-lookup"><span data-stu-id="b93a7-119">Storage Account Share Name (Azure file share name)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: StorageAccountShareName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b93a7-120">-DefaultProfile</span></span>
<span data-ttu-id="b93a7-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b93a7-122">-Name</span><span class="sxs-lookup"><span data-stu-id="b93a7-122">-Name</span></span>
<span data-ttu-id="b93a7-123">클라우드 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="b93a7-124">Azure Portal을 통해 만들면 이름이 참조하는 Azure 파일 공유의 이름으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: CloudEndpointName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="b93a7-125">-ParentObject</span></span>
<span data-ttu-id="b93a7-126">일반적으로 매개 변수를 통해 전달되는 SyncGroup 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-126">SyncGroup Object, normally passed through the parameter.</span></span>

```yaml
Type: Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup
Parameter Sets: ObjectParameterSet
Aliases: SyncGroup

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="b93a7-127">-ParentResourceId</span></span>
<span data-ttu-id="b93a7-128">SyncGroup 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b93a7-128">SyncGroup Parent Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ParentStringParameterSet
Aliases: SyncGroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b93a7-129">-ResourceGroupName</span></span>
<span data-ttu-id="b93a7-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="b93a7-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="b93a7-132">Storage 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="b93a7-132">Storage Account Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="b93a7-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="b93a7-134">Storage 계정 테넌트 ID(회사 디렉터리 ID)</span><span class="sxs-lookup"><span data-stu-id="b93a7-134">Storage Account Tenant Id (Company Directory Id)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="b93a7-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="b93a7-136">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-136">Name of the StorageSyncService.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases: ParentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="b93a7-137">-SyncGroupName</span></span>
<span data-ttu-id="b93a7-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-138">Name of the SyncGroup.</span></span>

```yaml
Type: System.String
Parameter Sets: StringParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b93a7-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b93a7-139">-Confirm</span></span>
<span data-ttu-id="b93a7-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b93a7-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b93a7-141">-WhatIf</span></span>
<span data-ttu-id="b93a7-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b93a7-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b93a7-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b93a7-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b93a7-144">CommonParameters</span></span>
<span data-ttu-id="b93a7-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b93a7-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b93a7-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="b93a7-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b93a7-147">입력</span><span class="sxs-lookup"><span data-stu-id="b93a7-147">INPUTS</span></span>

### <span data-ttu-id="b93a7-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="b93a7-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="b93a7-149">System.String</span><span class="sxs-lookup"><span data-stu-id="b93a7-149">System.String</span></span>

## <span data-ttu-id="b93a7-150">출력</span><span class="sxs-lookup"><span data-stu-id="b93a7-150">OUTPUTS</span></span>

### <span data-ttu-id="b93a7-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="b93a7-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="b93a7-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b93a7-152">NOTES</span></span>

## <span data-ttu-id="b93a7-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b93a7-153">RELATED LINKS</span></span>
