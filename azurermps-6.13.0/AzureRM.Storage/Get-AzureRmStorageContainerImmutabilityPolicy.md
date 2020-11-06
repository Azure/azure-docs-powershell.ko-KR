---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/get-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Get-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: cff5f387b6729f51634ee0466b099e1df8314589
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535051"
---
# <span data-ttu-id="62d76-101">Get-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="62d76-101">Get-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="62d76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62d76-102">SYNOPSIS</span></span>
<span data-ttu-id="62d76-103">저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62d76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="62d76-104">SYNTAX</span></span>

### <span data-ttu-id="62d76-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="62d76-105">AccountName (Default)</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62d76-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="62d76-106">AccountObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62d76-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="62d76-107">ContainerObject</span></span>
```
Get-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62d76-108">설명은</span><span class="sxs-lookup"><span data-stu-id="62d76-108">DESCRIPTION</span></span>
<span data-ttu-id="62d76-109">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet은 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-109">The **Get-AzureRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="62d76-110">예제의</span><span class="sxs-lookup"><span data-stu-id="62d76-110">EXAMPLES</span></span>

### <span data-ttu-id="62d76-111">예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 가져오기</span><span class="sxs-lookup"><span data-stu-id="62d76-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="62d76-112">이 명령은 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="62d76-113">예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy 가져오기</span><span class="sxs-lookup"><span data-stu-id="62d76-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="62d76-114">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="62d76-115">예제 3: 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 가져오기</span><span class="sxs-lookup"><span data-stu-id="62d76-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject 
```

<span data-ttu-id="62d76-116">이 명령은 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="62d76-117">변수</span><span class="sxs-lookup"><span data-stu-id="62d76-117">PARAMETERS</span></span>

### <span data-ttu-id="62d76-118">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="62d76-118">-Container</span></span>
<span data-ttu-id="62d76-119">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="62d76-119">Storage container object</span></span>

```yaml
Type: PSContainer
Parameter Sets: ContainerObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d76-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="62d76-120">-ContainerName</span></span>
<span data-ttu-id="62d76-121">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="62d76-121">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="62d76-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62d76-122">-DefaultProfile</span></span>
<span data-ttu-id="62d76-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62d76-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="62d76-124">-Etag</span></span>
<span data-ttu-id="62d76-125">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="62d76-125">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62d76-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62d76-126">-ResourceGroupName</span></span>
<span data-ttu-id="62d76-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="62d76-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="62d76-128">-StorageAccount</span></span>
<span data-ttu-id="62d76-129">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="62d76-129">Storage account object</span></span>

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

### <span data-ttu-id="62d76-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="62d76-130">-StorageAccountName</span></span>
<span data-ttu-id="62d76-131">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-131">Storage Account Name.</span></span>

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

### <span data-ttu-id="62d76-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62d76-132">CommonParameters</span></span>
<span data-ttu-id="62d76-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62d76-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62d76-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62d76-135">입력</span><span class="sxs-lookup"><span data-stu-id="62d76-135">INPUTS</span></span>

### <span data-ttu-id="62d76-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="62d76-136">System.String</span></span>

## <span data-ttu-id="62d76-137">출력</span><span class="sxs-lookup"><span data-stu-id="62d76-137">OUTPUTS</span></span>

### <span data-ttu-id="62d76-138">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="62d76-138">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="62d76-139">상속자</span><span class="sxs-lookup"><span data-stu-id="62d76-139">NOTES</span></span>

## <span data-ttu-id="62d76-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62d76-140">RELATED LINKS</span></span>

