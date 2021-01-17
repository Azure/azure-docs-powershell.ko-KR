---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: fb44ca997fd3b7599c25c5ba986ed0ca0771b3e6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98490755"
---
# <span data-ttu-id="25ff9-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="25ff9-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="25ff9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="25ff9-102">SYNOPSIS</span></span>
<span data-ttu-id="25ff9-103">Azure Redis Cache에서 컨테이너로 데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="25ff9-104">구문</span><span class="sxs-lookup"><span data-stu-id="25ff9-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="25ff9-105">설명</span><span class="sxs-lookup"><span data-stu-id="25ff9-105">DESCRIPTION</span></span>
<span data-ttu-id="25ff9-106">**Export-AzRedisCache** cmdlet은 Azure Redis Cache에서 컨테이너로 데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="25ff9-107">예제</span><span class="sxs-lookup"><span data-stu-id="25ff9-107">EXAMPLES</span></span>

### <span data-ttu-id="25ff9-108">예제 1: 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="25ff9-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="25ff9-109">이 명령은 Azure Redis Cache 인스턴스에서 SAS URL로 지정된 컨테이너로 데이터를 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="25ff9-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="25ff9-110">PARAMETERS</span></span>

### <span data-ttu-id="25ff9-111">-Container</span><span class="sxs-lookup"><span data-stu-id="25ff9-111">-Container</span></span>
<span data-ttu-id="25ff9-112">이 cmdlet이 데이터를 내보내는 컨테이너의 서비스 SAS URL을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="25ff9-113">$storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now)을 사용하여 서비스 SAS URL을 생성할 수 있습니다. AddMinutes(-15) -ExpiryTime([System.DateTime]::Now). AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="25ff9-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ff9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25ff9-114">-DefaultProfile</span></span>
<span data-ttu-id="25ff9-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="25ff9-116">-Format</span><span class="sxs-lookup"><span data-stu-id="25ff9-116">-Format</span></span>
<span data-ttu-id="25ff9-117">Blob의 형식을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="25ff9-118">현재 rdb는 지원되는 유일한 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-118">Currently rdb is the only supported format.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ff9-119">-Name</span><span class="sxs-lookup"><span data-stu-id="25ff9-119">-Name</span></span>
<span data-ttu-id="25ff9-120">캐시의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-120">Specifies the name of a cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ff9-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="25ff9-121">-PassThru</span></span>
<span data-ttu-id="25ff9-122">이 cmdlet은 작업이 성공하는지 여부를 나타내는 부울을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="25ff9-123">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="25ff9-124">-Prefix</span><span class="sxs-lookup"><span data-stu-id="25ff9-124">-Prefix</span></span>
<span data-ttu-id="25ff9-125">Blob 이름에 사용할 Prefix를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-125">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ff9-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="25ff9-126">-ResourceGroupName</span></span>
<span data-ttu-id="25ff9-127">캐시를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-127">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="25ff9-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="25ff9-128">-Confirm</span></span>
<span data-ttu-id="25ff9-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25ff9-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25ff9-130">-WhatIf</span></span>
<span data-ttu-id="25ff9-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="25ff9-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="25ff9-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25ff9-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25ff9-133">CommonParameters</span></span>
<span data-ttu-id="25ff9-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="25ff9-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25ff9-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="25ff9-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25ff9-136">입력</span><span class="sxs-lookup"><span data-stu-id="25ff9-136">INPUTS</span></span>

### <span data-ttu-id="25ff9-137">System.String</span><span class="sxs-lookup"><span data-stu-id="25ff9-137">System.String</span></span>

## <span data-ttu-id="25ff9-138">출력</span><span class="sxs-lookup"><span data-stu-id="25ff9-138">OUTPUTS</span></span>

### <span data-ttu-id="25ff9-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="25ff9-139">System.Boolean</span></span>

## <span data-ttu-id="25ff9-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="25ff9-140">NOTES</span></span>
* <span data-ttu-id="25ff9-141">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, redis, 캐시, 웹, 웹앱, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="25ff9-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="25ff9-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="25ff9-142">RELATED LINKS</span></span>

[<span data-ttu-id="25ff9-143">Import-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="25ff9-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="25ff9-144">New-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="25ff9-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="25ff9-145">Remove-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="25ff9-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="25ff9-146">Reset-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="25ff9-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="25ff9-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="25ff9-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


