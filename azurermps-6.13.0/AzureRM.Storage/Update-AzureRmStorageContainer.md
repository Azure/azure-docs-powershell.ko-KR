---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/update-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Update-AzureRmStorageContainer.md
ms.openlocfilehash: 9e4f62ef28d4cbcb22ddb563e558ad5d48733360
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531306"
---
# <span data-ttu-id="9efd2-101">Update-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="9efd2-101">Update-AzureRmStorageContainer</span></span>

## <span data-ttu-id="9efd2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9efd2-102">SYNOPSIS</span></span>
<span data-ttu-id="9efd2-103">저장소 blob 컨테이너 수정</span><span class="sxs-lookup"><span data-stu-id="9efd2-103">Modifies a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9efd2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9efd2-104">SYNTAX</span></span>

### <span data-ttu-id="9efd2-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9efd2-105">AccountName (Default)</span></span>
```
Update-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9efd2-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="9efd2-106">AccountObject</span></span>
```
Update-AzureRmStorageContainer [-Name] <String> -StorageAccount <PSStorageAccount>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9efd2-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="9efd2-107">ContainerObject</span></span>
```
Update-AzureRmStorageContainer -InputObject <PSContainer> [-PublicAccess <PSPublicAccess>]
 [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9efd2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9efd2-108">DESCRIPTION</span></span>
<span data-ttu-id="9efd2-109">**업데이트 AzureRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-109">The **Update-AzureRmStorageContainer** cmdlet modifies a Storage blob container</span></span>

## <span data-ttu-id="9efd2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="9efd2-110">EXAMPLES</span></span>

### <span data-ttu-id="9efd2-111">예제 1: 저장소 blob 컨테이너의 메타 데이터 및 저장소 계정 이름과 컨테이너 이름을 사용 하 여 공용 액세스 수정</span><span class="sxs-lookup"><span data-stu-id="9efd2-111">Example 1: Modifies a Storage blob container's metadata and public access with Storage account name and container name</span></span>
```
PS C:\>Update-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -PublicAccess Container -Metadata @{tag0="value0";tag1="value1"} 
```

<span data-ttu-id="9efd2-112">이 명령은 저장소 blob 컨테이너의 메타 데이터 및 저장소 계정 이름과 컨테이너 이름을 사용 하 여 공용 액세스를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-112">This command modifies a Storage blob container's metadata and public access with Storage account name and container name.</span></span>

### <span data-ttu-id="9efd2-113">예제 2: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 공용 액세스 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9efd2-113">Example 2: Disable public access on a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Update-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess None
```

<span data-ttu-id="9efd2-114">이 명령은 저장소 계정 개체와 컨테이너 이름을 가진 저장소 blob 컨테이너에서 공용 액세스를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-114">This command disables public access on a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="9efd2-115">예제 3: 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너에 대 한 Blob로 공용 액세스 설정</span><span class="sxs-lookup"><span data-stu-id="9efd2-115">Example 3: Set public access as Blob for all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Update-AzureRmStorageContainer -PublicAccess Blob
```

<span data-ttu-id="9efd2-116">이 명령은 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너에 대해 공용 액세스를 Blob로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-116">This command set public access as Blob for all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="9efd2-117">변수</span><span class="sxs-lookup"><span data-stu-id="9efd2-117">PARAMETERS</span></span>

### <span data-ttu-id="9efd2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9efd2-118">-DefaultProfile</span></span>
<span data-ttu-id="9efd2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9efd2-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9efd2-120">-InputObject</span></span>
<span data-ttu-id="9efd2-121">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="9efd2-121">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-122">-Metadata</span><span class="sxs-lookup"><span data-stu-id="9efd2-122">-Metadata</span></span>
<span data-ttu-id="9efd2-123">컨테이너 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="9efd2-123">Container Metadata</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-124">-이름</span><span class="sxs-lookup"><span data-stu-id="9efd2-124">-Name</span></span>
<span data-ttu-id="9efd2-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="9efd2-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-126">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="9efd2-126">-PublicAccess</span></span>
<span data-ttu-id="9efd2-127">컨테이너 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="9efd2-127">Container PublicAccess</span></span>

```yaml
Type: PSPublicAccess
Parameter Sets: (All)
Aliases: 
Accepted values: Container, Blob

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9efd2-128">-ResourceGroupName</span></span>
<span data-ttu-id="9efd2-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-129">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="9efd2-130">-StorageAccount</span></span>
<span data-ttu-id="9efd2-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="9efd2-131">Storage account object</span></span>

```yaml
Type: PSStorageAccount
Parameter Sets: AccountObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="9efd2-132">-StorageAccountName</span></span>
<span data-ttu-id="9efd2-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-133">Storage Account Name.</span></span>

```yaml
Type: String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9efd2-134">-확인</span><span class="sxs-lookup"><span data-stu-id="9efd2-134">-Confirm</span></span>
<span data-ttu-id="9efd2-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9efd2-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9efd2-136">-WhatIf</span></span>
<span data-ttu-id="9efd2-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9efd2-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9efd2-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9efd2-139">CommonParameters</span></span>
<span data-ttu-id="9efd2-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9efd2-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9efd2-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9efd2-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9efd2-142">입력</span><span class="sxs-lookup"><span data-stu-id="9efd2-142">INPUTS</span></span>

### <span data-ttu-id="9efd2-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9efd2-143">System.String</span></span>

## <span data-ttu-id="9efd2-144">출력</span><span class="sxs-lookup"><span data-stu-id="9efd2-144">OUTPUTS</span></span>

### <span data-ttu-id="9efd2-145">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="9efd2-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="9efd2-146">상속자</span><span class="sxs-lookup"><span data-stu-id="9efd2-146">NOTES</span></span>

## <span data-ttu-id="9efd2-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9efd2-147">RELATED LINKS</span></span>

