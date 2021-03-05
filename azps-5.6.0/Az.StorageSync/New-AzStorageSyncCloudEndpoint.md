---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StorageSync.dll-Help.xml
Module Name: Az.StorageSync
online version: https://docs.microsoft.com/powershell/module/Az.storagesync/new-Azstoragesynccloudendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StorageSync/StorageSync/help/New-AzStorageSyncCloudEndpoint.md
ms.openlocfilehash: c55b49052ae34eba9dfff960c85e9ade7617d2a3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102011419"
---
# <span data-ttu-id="27cb1-101">New-AzStorageSyncCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="27cb1-101">New-AzStorageSyncCloudEndpoint</span></span>

## <span data-ttu-id="27cb1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="27cb1-102">SYNOPSIS</span></span>
<span data-ttu-id="27cb1-103">이 명령은 동기화 그룹에 Azure 파일 동기화 클라우드 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-103">This command creates an Azure File Sync cloud endpoint in a sync group.</span></span>

## <span data-ttu-id="27cb1-104">구문</span><span class="sxs-lookup"><span data-stu-id="27cb1-104">SYNTAX</span></span>

### <span data-ttu-id="27cb1-105">StringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="27cb1-105">StringParameterSet (Default)</span></span>
```
New-AzStorageSyncCloudEndpoint [-ResourceGroupName] <String> [-StorageSyncServiceName] <String>
 [-SyncGroupName] <String> -Name <String> -StorageAccountResourceId <String> -AzureFileShareName <String>
 [-StorageAccountTenantId <String>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="27cb1-106">ObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="27cb1-106">ObjectParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentObject] <PSSyncGroup> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="27cb1-107">ParentStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="27cb1-107">ParentStringParameterSet</span></span>
```
New-AzStorageSyncCloudEndpoint [-ParentResourceId] <String> -Name <String> -StorageAccountResourceId <String>
 -AzureFileShareName <String> [-StorageAccountTenantId <String>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="27cb1-108">설명</span><span class="sxs-lookup"><span data-stu-id="27cb1-108">DESCRIPTION</span></span>
<span data-ttu-id="27cb1-109">이 명령은 Azure 파일 동기화 클라우드 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-109">This command creates an Azure File Sync cloud endpoint.</span></span> <span data-ttu-id="27cb1-110">클라우드 엔드포인트는 기존 Azure 파일 공유에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-110">A cloud endpoint is a reference to an existing Azure file share.</span></span> <span data-ttu-id="27cb1-111">파일 공유를 나타내고 클라우드 엔드포인트가 만든 동기화 그룹의 모든 파일 부분을 동기화하는 참여를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-111">It represents the file share and defines it participation in syncing all the files part of the sync group the cloud endpoint has been created in.</span></span>

## <span data-ttu-id="27cb1-112">예제</span><span class="sxs-lookup"><span data-stu-id="27cb1-112">EXAMPLES</span></span>

### <span data-ttu-id="27cb1-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="27cb1-113">Example 1</span></span>
```powershell
PS C:\> New-AzStorageSyncCloudEndpoint -ResourceGroupName "myResourceGroup" -StorageSyncServiceName "myStorageSyncServiceName" -SyncGroupName "mySyncGroupName" -Name "myCloudEndpointName" -StorageAccountResourceId $storageAccountResourceId -AzureFileShareName "myAzureFileShareName" -StorageAccountTenantId "myStorageAccountTenantId"
```

<span data-ttu-id="27cb1-114">클라우드 엔드포인트는 동기화 그룹의 통합 멤버입니다. 이는 "mySyncGroupName"이라는 기존 동기화 그룹의 내부를 만드는 예제입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-114">A cloud endpoint is an integral member of a sync group, this is an example of creating one inside of an existing sync group called "mySyncGroupName".</span></span>

## <span data-ttu-id="27cb1-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="27cb1-115">PARAMETERS</span></span>

### <span data-ttu-id="27cb1-116">-AsJob</span><span class="sxs-lookup"><span data-stu-id="27cb1-116">-AsJob</span></span>
<span data-ttu-id="27cb1-117">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="27cb1-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="27cb1-118">-AzureFileShareName</span><span class="sxs-lookup"><span data-stu-id="27cb1-118">-AzureFileShareName</span></span>
<span data-ttu-id="27cb1-119">Storage 계정 공유 이름(Azure 파일 공유 이름)</span><span class="sxs-lookup"><span data-stu-id="27cb1-119">Storage Account Share Name (Azure file share name)</span></span>

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

### <span data-ttu-id="27cb1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="27cb1-120">-DefaultProfile</span></span>
<span data-ttu-id="27cb1-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="27cb1-122">-Name</span><span class="sxs-lookup"><span data-stu-id="27cb1-122">-Name</span></span>
<span data-ttu-id="27cb1-123">클라우드 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-123">Name of the cloud endpoint.</span></span> <span data-ttu-id="27cb1-124">Azure Portal을 통해 만들 때 이름이 참조하는 Azure 파일 공유의 이름으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-124">When created through the Azure portal, Name is set to the name of the Azure file share it references.</span></span>

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

### <span data-ttu-id="27cb1-125">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="27cb1-125">-ParentObject</span></span>
<span data-ttu-id="27cb1-126">SyncGroup 개체( 일반적으로 매개 변수를 통과합니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-126">SyncGroup Object, normally passed through the parameter.</span></span>

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

### <span data-ttu-id="27cb1-127">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="27cb1-127">-ParentResourceId</span></span>
<span data-ttu-id="27cb1-128">SyncGroup 부모 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="27cb1-128">SyncGroup Parent Resource Id</span></span>

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

### <span data-ttu-id="27cb1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="27cb1-129">-ResourceGroupName</span></span>
<span data-ttu-id="27cb1-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="27cb1-131">-StorageAccountResourceId</span><span class="sxs-lookup"><span data-stu-id="27cb1-131">-StorageAccountResourceId</span></span>
<span data-ttu-id="27cb1-132">Storage 계정 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="27cb1-132">Storage Account Resource Id</span></span>

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

### <span data-ttu-id="27cb1-133">-StorageAccountTenantId</span><span class="sxs-lookup"><span data-stu-id="27cb1-133">-StorageAccountTenantId</span></span>
<span data-ttu-id="27cb1-134">Storage 계정 테넌트 ID(회사 디렉터리 ID)</span><span class="sxs-lookup"><span data-stu-id="27cb1-134">Storage Account Tenant Id (Company Directory Id)</span></span>

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

### <span data-ttu-id="27cb1-135">-StorageSyncServiceName</span><span class="sxs-lookup"><span data-stu-id="27cb1-135">-StorageSyncServiceName</span></span>
<span data-ttu-id="27cb1-136">StorageSyncService의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-136">Name of the StorageSyncService.</span></span>

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

### <span data-ttu-id="27cb1-137">-SyncGroupName</span><span class="sxs-lookup"><span data-stu-id="27cb1-137">-SyncGroupName</span></span>
<span data-ttu-id="27cb1-138">SyncGroup의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-138">Name of the SyncGroup.</span></span>

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

### <span data-ttu-id="27cb1-139">-확인</span><span class="sxs-lookup"><span data-stu-id="27cb1-139">-Confirm</span></span>
<span data-ttu-id="27cb1-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="27cb1-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="27cb1-141">-WhatIf</span></span>
<span data-ttu-id="27cb1-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-142">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="27cb1-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="27cb1-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="27cb1-144">CommonParameters</span></span>
<span data-ttu-id="27cb1-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="27cb1-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="27cb1-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="27cb1-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="27cb1-147">입력</span><span class="sxs-lookup"><span data-stu-id="27cb1-147">INPUTS</span></span>

### <span data-ttu-id="27cb1-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span><span class="sxs-lookup"><span data-stu-id="27cb1-148">Microsoft.Azure.Commands.StorageSync.Models.PSSyncGroup</span></span>

### <span data-ttu-id="27cb1-149">System.String</span><span class="sxs-lookup"><span data-stu-id="27cb1-149">System.String</span></span>

## <span data-ttu-id="27cb1-150">출력</span><span class="sxs-lookup"><span data-stu-id="27cb1-150">OUTPUTS</span></span>

### <span data-ttu-id="27cb1-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span><span class="sxs-lookup"><span data-stu-id="27cb1-151">Microsoft.Azure.Commands.StorageSync.Models.PSCloudEndpoint</span></span>

## <span data-ttu-id="27cb1-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="27cb1-152">NOTES</span></span>

## <span data-ttu-id="27cb1-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="27cb1-153">RELATED LINKS</span></span>
