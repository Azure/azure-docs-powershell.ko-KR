---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/new-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/New-AzureRmStorageContainer.md
ms.openlocfilehash: 8e136188a2857b53b566d30c439e222caea16abb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525963"
---
# <span data-ttu-id="6124c-101">New-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="6124c-101">New-AzureRmStorageContainer</span></span>

## <span data-ttu-id="6124c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6124c-102">SYNOPSIS</span></span>
<span data-ttu-id="6124c-103">저장소 blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-103">Creates a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6124c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6124c-104">SYNTAX</span></span>

### <span data-ttu-id="6124c-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="6124c-105">AccountName (Default)</span></span>
```
New-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6124c-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="6124c-106">AccountObject</span></span>
```
New-AzureRmStorageContainer -StorageAccount <PSStorageAccount> [-Name] <String>
 [-PublicAccess <PSPublicAccess>] [-Metadata <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6124c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6124c-107">DESCRIPTION</span></span>
<span data-ttu-id="6124c-108">**새 AzureRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-108">The **New-AzureRmStorageContainer** cmdlet creates a Storage blob container</span></span>

## <span data-ttu-id="6124c-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6124c-109">EXAMPLES</span></span>

### <span data-ttu-id="6124c-110">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너 만들기 (메타 데이터 포함)</span><span class="sxs-lookup"><span data-stu-id="6124c-110">Example 1: Create a Storage blob container with Storage account name and container name, with metadata</span></span>
```
PS C:\>New-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Metadata @{tag0="value0";tag1="value1";tag2="value2"} 
```

<span data-ttu-id="6124c-111">이 명령은 저장소 계정 이름과 컨테이너 이름으로 메타 데이터를 사용 하 여 저장소 blob 컨테이너를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-111">This command creates a Storage blob container with Storage account name and container name, with metadata.</span></span>

### <span data-ttu-id="6124c-112">예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너 만들기 (Blob로 공용 액세스 사용)</span><span class="sxs-lookup"><span data-stu-id="6124c-112">Example 2: Create a Storage blob container with Storage account object and container name, with public access as Blob</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>New-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer" -PublicAccess Blob
```

<span data-ttu-id="6124c-113">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너를 만들고 공용 액세스를 Blob로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-113">This command creates a Storage blob container with Storage account object and container name, with public access as Blob.</span></span>

## <span data-ttu-id="6124c-114">변수</span><span class="sxs-lookup"><span data-stu-id="6124c-114">PARAMETERS</span></span>

### <span data-ttu-id="6124c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6124c-115">-DefaultProfile</span></span>
<span data-ttu-id="6124c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6124c-117">-Metadata</span><span class="sxs-lookup"><span data-stu-id="6124c-117">-Metadata</span></span>
<span data-ttu-id="6124c-118">컨테이너 메타 데이터</span><span class="sxs-lookup"><span data-stu-id="6124c-118">Container Metadata</span></span>

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

### <span data-ttu-id="6124c-119">-이름</span><span class="sxs-lookup"><span data-stu-id="6124c-119">-Name</span></span>
<span data-ttu-id="6124c-120">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="6124c-120">Container Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: N, ContainerName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6124c-121">-PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6124c-121">-PublicAccess</span></span>
<span data-ttu-id="6124c-122">컨테이너 PublicAccess</span><span class="sxs-lookup"><span data-stu-id="6124c-122">Container PublicAccess</span></span>

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

### <span data-ttu-id="6124c-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6124c-123">-ResourceGroupName</span></span>
<span data-ttu-id="6124c-124">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-124">Resource Group Name.</span></span>

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

### <span data-ttu-id="6124c-125">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="6124c-125">-StorageAccount</span></span>
<span data-ttu-id="6124c-126">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="6124c-126">Storage account object</span></span>

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

### <span data-ttu-id="6124c-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="6124c-127">-StorageAccountName</span></span>
<span data-ttu-id="6124c-128">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-128">Storage Account Name.</span></span>

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

### <span data-ttu-id="6124c-129">-확인</span><span class="sxs-lookup"><span data-stu-id="6124c-129">-Confirm</span></span>
<span data-ttu-id="6124c-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6124c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6124c-131">-WhatIf</span></span>
<span data-ttu-id="6124c-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6124c-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6124c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6124c-134">CommonParameters</span></span>
<span data-ttu-id="6124c-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6124c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6124c-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6124c-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6124c-137">입력</span><span class="sxs-lookup"><span data-stu-id="6124c-137">INPUTS</span></span>

### <span data-ttu-id="6124c-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6124c-138">System.String</span></span>

## <span data-ttu-id="6124c-139">출력</span><span class="sxs-lookup"><span data-stu-id="6124c-139">OUTPUTS</span></span>

### <span data-ttu-id="6124c-140">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="6124c-140">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="6124c-141">상속자</span><span class="sxs-lookup"><span data-stu-id="6124c-141">NOTES</span></span>

## <span data-ttu-id="6124c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6124c-142">RELATED LINKS</span></span>

