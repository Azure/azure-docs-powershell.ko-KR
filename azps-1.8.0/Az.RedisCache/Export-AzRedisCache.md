---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RedisCache.dll-Help.xml
Module Name: Az.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/az.rediscache/export-azrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RedisCache/RedisCache/help/Export-AzRedisCache.md
ms.openlocfilehash: ec6abf13cf4f14a8d0cdaab75d5816d87f0540ad
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699564"
---
# <span data-ttu-id="ef035-101">Export-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef035-101">Export-AzRedisCache</span></span>

## <span data-ttu-id="ef035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef035-102">SYNOPSIS</span></span>
<span data-ttu-id="ef035-103">Azure Redis Cache에서 컨테이너로 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-103">Exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="ef035-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef035-104">SYNTAX</span></span>

```
Export-AzRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ef035-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef035-105">DESCRIPTION</span></span>
<span data-ttu-id="ef035-106">**Export-AzRedisCache** Cmdlet은 Azure Redis Cache에서 컨테이너로 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-106">The **Export-AzRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="ef035-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef035-107">EXAMPLES</span></span>

### <span data-ttu-id="ef035-108">예제 1: 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="ef035-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="ef035-109">이 명령은 Azure Redis Cache 인스턴스에서 SAS URL로 지정 된 컨테이너로 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="ef035-110">변수</span><span class="sxs-lookup"><span data-stu-id="ef035-110">PARAMETERS</span></span>

### <span data-ttu-id="ef035-111">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="ef035-111">-Container</span></span>
<span data-ttu-id="ef035-112">이 cmdlet이 데이터를 내보내는 컨테이너의 서비스 SA URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="ef035-113">다음 PowerShell 명령을 사용 하 여 서비스 SA URL을 생성할 수 있습니다. $storageAccountContext = New-AzStorageContext-StorageAccountName "storageName"-StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken-이름 "containername"-Permission "rwdl"-StartTime ([System: DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri Export-AzRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Prefix "blobprefix"-컨테이너 ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="ef035-113">You can generate a Service SAS URL using the following PowerShell commands: $storageAccountContext = New-AzStorageContext -StorageAccountName "storageName" -StorageAccountKey "key" $sasKeyForContainer = New-AzStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri Export-AzRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

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

### <span data-ttu-id="ef035-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef035-114">-DefaultProfile</span></span>
<span data-ttu-id="ef035-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ef035-116">-형식</span><span class="sxs-lookup"><span data-stu-id="ef035-116">-Format</span></span>
<span data-ttu-id="ef035-117">Blob에 대 한 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-117">Specifies a format for the blob.</span></span>
<span data-ttu-id="ef035-118">현재 rdb만 지원 되는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-118">Currently rdb is the only supported format.</span></span>

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

### <span data-ttu-id="ef035-119">-이름</span><span class="sxs-lookup"><span data-stu-id="ef035-119">-Name</span></span>
<span data-ttu-id="ef035-120">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-120">Specifies the name of a cache.</span></span>

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

### <span data-ttu-id="ef035-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="ef035-121">-PassThru</span></span>
<span data-ttu-id="ef035-122">이 cmdlet이 작업 성공 여부를 나타내는 Boolean을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-122">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="ef035-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="ef035-124">-접두사</span><span class="sxs-lookup"><span data-stu-id="ef035-124">-Prefix</span></span>
<span data-ttu-id="ef035-125">Blob 이름에 사용할 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-125">Specifies a prefix to use for blob names.</span></span>

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

### <span data-ttu-id="ef035-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ef035-126">-ResourceGroupName</span></span>
<span data-ttu-id="ef035-127">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-127">Specifies the name of the resource group that contains the cache.</span></span>

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

### <span data-ttu-id="ef035-128">-확인</span><span class="sxs-lookup"><span data-stu-id="ef035-128">-Confirm</span></span>
<span data-ttu-id="ef035-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef035-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef035-130">-WhatIf</span></span>
<span data-ttu-id="ef035-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef035-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef035-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef035-133">CommonParameters</span></span>
<span data-ttu-id="ef035-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef035-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef035-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef035-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef035-136">입력</span><span class="sxs-lookup"><span data-stu-id="ef035-136">INPUTS</span></span>

### <span data-ttu-id="ef035-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ef035-137">System.String</span></span>

## <span data-ttu-id="ef035-138">출력</span><span class="sxs-lookup"><span data-stu-id="ef035-138">OUTPUTS</span></span>

### <span data-ttu-id="ef035-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="ef035-139">System.Boolean</span></span>

## <span data-ttu-id="ef035-140">상속자</span><span class="sxs-lookup"><span data-stu-id="ef035-140">NOTES</span></span>
* <span data-ttu-id="ef035-141">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="ef035-141">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="ef035-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef035-142">RELATED LINKS</span></span>

[<span data-ttu-id="ef035-143">가져오기-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef035-143">Import-AzRedisCache</span></span>](./Import-AzRedisCache.md)

[<span data-ttu-id="ef035-144">새로운 AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef035-144">New-AzRedisCache</span></span>](./New-AzRedisCache.md)

[<span data-ttu-id="ef035-145">제거-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef035-145">Remove-AzRedisCache</span></span>](./Remove-AzRedisCache.md)

[<span data-ttu-id="ef035-146">다시 설정-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef035-146">Reset-AzRedisCache</span></span>](./Reset-AzRedisCache.md)

[<span data-ttu-id="ef035-147">Set-AzRedisCache</span><span class="sxs-lookup"><span data-stu-id="ef035-147">Set-AzRedisCache</span></span>](./Set-AzRedisCache.md)


