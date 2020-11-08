---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 2a1dee58ba741e5bd1c1122b704c5d62666338f2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226486"
---
# <span data-ttu-id="230f0-101">Get-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="230f0-101">Get-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="230f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="230f0-102">SYNOPSIS</span></span>
<span data-ttu-id="230f0-103">저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-103">Gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="230f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="230f0-104">SYNTAX</span></span>

### <span data-ttu-id="230f0-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="230f0-105">AccountName (Default)</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230f0-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="230f0-106">AccountObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="230f0-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="230f0-107">ContainerObject</span></span>
```
Get-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="230f0-108">설명은</span><span class="sxs-lookup"><span data-stu-id="230f0-108">DESCRIPTION</span></span>
<span data-ttu-id="230f0-109">**AzRmStorageContainerImmutabilityPolicy** Cmdlet은 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-109">The **Get-AzRmStorageContainerImmutabilityPolicy** cmdlet gets ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="230f0-110">예제의</span><span class="sxs-lookup"><span data-stu-id="230f0-110">EXAMPLES</span></span>

### <span data-ttu-id="230f0-111">예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 가져오기</span><span class="sxs-lookup"><span data-stu-id="230f0-111">Example 1: Get ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="230f0-112">이 명령은 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-112">This command gets ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="230f0-113">예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy 가져오기</span><span class="sxs-lookup"><span data-stu-id="230f0-113">Example 2: Get ImmutabilityPolicy of a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="230f0-114">이 명령은 저장소 계정 개체와 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-114">This command gets ImmutabilityPolicy of a Storage blob containers with Storage account object and container name.</span></span>

### <span data-ttu-id="230f0-115">예제 3: 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 가져오기</span><span class="sxs-lookup"><span data-stu-id="230f0-115">Example 3: Get ImmutabilityPolicy of a Storage blob container with Storage container object</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -Container $containerObject
```

<span data-ttu-id="230f0-116">이 명령은 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-116">This command gets ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

## <span data-ttu-id="230f0-117">변수</span><span class="sxs-lookup"><span data-stu-id="230f0-117">PARAMETERS</span></span>

### <span data-ttu-id="230f0-118">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="230f0-118">-Container</span></span>
<span data-ttu-id="230f0-119">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="230f0-119">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="230f0-120">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="230f0-120">-ContainerName</span></span>
<span data-ttu-id="230f0-121">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="230f0-121">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="230f0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="230f0-122">-DefaultProfile</span></span>
<span data-ttu-id="230f0-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="230f0-124">-Etag</span><span class="sxs-lookup"><span data-stu-id="230f0-124">-Etag</span></span>
<span data-ttu-id="230f0-125">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="230f0-125">Immutability policy etag.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="230f0-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="230f0-126">-ResourceGroupName</span></span>
<span data-ttu-id="230f0-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-127">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="230f0-128">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="230f0-128">-StorageAccount</span></span>
<span data-ttu-id="230f0-129">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="230f0-129">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="230f0-130">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="230f0-130">-StorageAccountName</span></span>
<span data-ttu-id="230f0-131">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-131">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="230f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="230f0-132">CommonParameters</span></span>
<span data-ttu-id="230f0-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="230f0-134">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="230f0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="230f0-135">입력</span><span class="sxs-lookup"><span data-stu-id="230f0-135">INPUTS</span></span>

### <span data-ttu-id="230f0-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="230f0-136">System.String</span></span>

### <span data-ttu-id="230f0-137">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="230f0-137">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="230f0-138">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="230f0-138">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="230f0-139">출력</span><span class="sxs-lookup"><span data-stu-id="230f0-139">OUTPUTS</span></span>

### <span data-ttu-id="230f0-140">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="230f0-140">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="230f0-141">상속자</span><span class="sxs-lookup"><span data-stu-id="230f0-141">NOTES</span></span>

## <span data-ttu-id="230f0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="230f0-142">RELATED LINKS</span></span>
