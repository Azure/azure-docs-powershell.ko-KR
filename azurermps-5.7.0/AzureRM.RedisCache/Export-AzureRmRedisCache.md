---
external help file: Microsoft.Azure.Commands.RedisCache.dll-Help.xml
Module Name: AzureRM.RedisCache
ms.assetid: B447E492-D87E-4DA3-A8B0-0BAF603CCC26
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.rediscache/export-azurermrediscache
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RedisCache/Commands.RedisCache/help/Export-AzureRmRedisCache.md
ms.openlocfilehash: cd19fe8052ae95f547971452f4364f279f365cac
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528861"
---
# <span data-ttu-id="7dd55-101">Export-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7dd55-101">Export-AzureRmRedisCache</span></span>

## <span data-ttu-id="7dd55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7dd55-102">SYNOPSIS</span></span>
<span data-ttu-id="7dd55-103">Azure Redis Cache에서 컨테이너로 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-103">Exports data from Azure Redis Cache to a container.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7dd55-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7dd55-104">SYNTAX</span></span>

```
Export-AzureRmRedisCache [-ResourceGroupName <String>] -Name <String> -Prefix <String> -Container <String>
 [-Format <String>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="7dd55-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7dd55-105">DESCRIPTION</span></span>
<span data-ttu-id="7dd55-106">**Export-AzureRmRedisCache** Cmdlet은 Azure Redis Cache에서 컨테이너로 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-106">The **Export-AzureRmRedisCache** cmdlet exports data from Azure Redis Cache to a container.</span></span>

## <span data-ttu-id="7dd55-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7dd55-107">EXAMPLES</span></span>

### <span data-ttu-id="7dd55-108">예제 1: 데이터 내보내기</span><span class="sxs-lookup"><span data-stu-id="7dd55-108">Example 1: Export data</span></span>
```
PS C:\>Export-AzureRmRedisCache -ResourceGroupName "ResourceGroup13" -Name "RedisCache06" -Prefix "blobprefix" -Container "https://mystorageaccount.blob.core.windows.net/container18?sv=2015-04-05&sr=c&sig=HezZtBZ3DURmEGDduauE7pvETY4kqlPI8JCNa8ATmaw%3D&st=2016-05-27T00%3A00%3A00Z&se=2016-05-28T00%3A00%3A00Z&sp=rwdl"
```

<span data-ttu-id="7dd55-109">이 명령은 Azure Redis Cache 인스턴스에서 SAS URL로 지정 된 컨테이너로 데이터를 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-109">This command exports data from an Azure Redis Cache instance into the container that is specified by the SAS URL.</span></span>

## <span data-ttu-id="7dd55-110">변수</span><span class="sxs-lookup"><span data-stu-id="7dd55-110">PARAMETERS</span></span>

### <span data-ttu-id="7dd55-111">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="7dd55-111">-Container</span></span>
<span data-ttu-id="7dd55-112">이 cmdlet이 데이터를 내보내는 컨테이너의 서비스 SA URL을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-112">Specifies the Service SAS URL of container where this cmdlet exports data.</span></span> <span data-ttu-id="7dd55-113">다음 PowerShell 명령을 사용 하 여 서비스 SAS URL을 생성할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-113">You can generate a Service SAS URL using the following PowerShell commands:</span></span>

<span data-ttu-id="7dd55-114">$storageAccountContext = New-AzureStorageContext-StorageAccountName "storageName"-StorageAccountKey "key"</span><span class="sxs-lookup"><span data-stu-id="7dd55-114">$storageAccountContext = New-AzureStorageContext -StorageAccountName "storageName" -StorageAccountKey "key"</span></span>

<span data-ttu-id="7dd55-115">$sasKeyForContainer = New-AzureStorageContainerSASToken-Name "containername"-권한 "rwdl"-StartTime ([System: DateTime]:: Now). AddMinutes (-15)-ExpiryTime ([System. DateTime]:: Now). AddHours (5)-Context $storageAccountContext-FullUri</span><span class="sxs-lookup"><span data-stu-id="7dd55-115">$sasKeyForContainer = New-AzureStorageContainerSASToken -Name "containername" -Permission "rwdl" -StartTime ([System.DateTime]::Now).AddMinutes(-15) -ExpiryTime ([System.DateTime]::Now).AddHours(5) -Context $storageAccountContext -FullUri</span></span> 

<span data-ttu-id="7dd55-116">Export-AzureRmRedisCache-ResourceGroupName "ResourceGroupName"-Name "cacheName"-Prefix "blobprefix"-컨테이너 ($sasKeyForContainer)</span><span class="sxs-lookup"><span data-stu-id="7dd55-116">Export-AzureRmRedisCache -ResourceGroupName "ResourceGroupName" -Name "cacheName" -Prefix "blobprefix" -Container ($sasKeyForContainer)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7dd55-117">-DefaultProfile</span></span>
<span data-ttu-id="7dd55-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-119">-형식</span><span class="sxs-lookup"><span data-stu-id="7dd55-119">-Format</span></span>
<span data-ttu-id="7dd55-120">Blob에 대 한 형식을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-120">Specifies a format for the blob.</span></span>
<span data-ttu-id="7dd55-121">현재 rdb만 지원 되는 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-121">Currently rdb is the only supported format.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-122">-이름</span><span class="sxs-lookup"><span data-stu-id="7dd55-122">-Name</span></span>
<span data-ttu-id="7dd55-123">캐시의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-123">Specifies the name of a cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7dd55-124">-PassThru</span></span>
<span data-ttu-id="7dd55-125">이 cmdlet이 작업 성공 여부를 나타내는 Boolean을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-125">Indicates that this cmdlet returns a Boolean that indicates whether the operation succeeds.</span></span>
<span data-ttu-id="7dd55-126">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-126">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-127">-접두사</span><span class="sxs-lookup"><span data-stu-id="7dd55-127">-Prefix</span></span>
<span data-ttu-id="7dd55-128">Blob 이름에 사용할 접두사를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-128">Specifies a prefix to use for blob names.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7dd55-129">-ResourceGroupName</span></span>
<span data-ttu-id="7dd55-130">캐시를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-130">Specifies the name of the resource group that contains the cache.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7dd55-131">-확인</span><span class="sxs-lookup"><span data-stu-id="7dd55-131">-Confirm</span></span>
<span data-ttu-id="7dd55-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7dd55-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7dd55-133">-WhatIf</span></span>
<span data-ttu-id="7dd55-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7dd55-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7dd55-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7dd55-136">CommonParameters</span></span>
<span data-ttu-id="7dd55-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7dd55-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7dd55-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7dd55-139">입력</span><span class="sxs-lookup"><span data-stu-id="7dd55-139">INPUTS</span></span>

### <span data-ttu-id="7dd55-140">않아야</span><span class="sxs-lookup"><span data-stu-id="7dd55-140">None</span></span>
<span data-ttu-id="7dd55-141">속성 이름으로이 cmdlet에 대 한 입력을 파이프로 지정할 수 있지만 값을 기준으로 하지 않아도 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7dd55-141">You can pipe input to this cmdlet by property name, but not by value.</span></span>

## <span data-ttu-id="7dd55-142">출력</span><span class="sxs-lookup"><span data-stu-id="7dd55-142">OUTPUTS</span></span>

### <span data-ttu-id="7dd55-143">않아야</span><span class="sxs-lookup"><span data-stu-id="7dd55-143">None</span></span>

## <span data-ttu-id="7dd55-144">상속자</span><span class="sxs-lookup"><span data-stu-id="7dd55-144">NOTES</span></span>
* <span data-ttu-id="7dd55-145">키워드: azure, azurerm, arm, resource, 관리, manager, redis, cache, web, web app, 웹 사이트</span><span class="sxs-lookup"><span data-stu-id="7dd55-145">Keywords: azure, azurerm, arm, resource, management, manager, redis, cache, web, webapp, website</span></span>

## <span data-ttu-id="7dd55-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7dd55-146">RELATED LINKS</span></span>

[<span data-ttu-id="7dd55-147">가져오기-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7dd55-147">Import-AzureRmRedisCache</span></span>](./Import-AzureRmRedisCache.md)

[<span data-ttu-id="7dd55-148">새로운 AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7dd55-148">New-AzureRmRedisCache</span></span>](./New-AzureRmRedisCache.md)

[<span data-ttu-id="7dd55-149">제거-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7dd55-149">Remove-AzureRmRedisCache</span></span>](./Remove-AzureRmRedisCache.md)

[<span data-ttu-id="7dd55-150">다시 설정-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7dd55-150">Reset-AzureRmRedisCache</span></span>](./Reset-AzureRmRedisCache.md)

[<span data-ttu-id="7dd55-151">Set-AzureRmRedisCache</span><span class="sxs-lookup"><span data-stu-id="7dd55-151">Set-AzureRmRedisCache</span></span>](./Set-AzureRmRedisCache.md)


