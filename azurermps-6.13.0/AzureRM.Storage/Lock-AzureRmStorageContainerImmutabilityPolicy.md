---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/lock-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Lock-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 726dc9043c1082f97e32da46305cf81192e1806c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524272"
---
# <span data-ttu-id="ce781-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="ce781-101">Lock-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="ce781-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce781-102">SYNOPSIS</span></span>
<span data-ttu-id="ce781-103">저장소 blob 컨테이너의 ImmutabilityPolicy 잠금</span><span class="sxs-lookup"><span data-stu-id="ce781-103">Locks ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ce781-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ce781-104">SYNTAX</span></span>

### <span data-ttu-id="ce781-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="ce781-105">AccountName (Default)</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce781-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="ce781-106">AccountObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce781-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="ce781-107">ContainerObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ce781-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="ce781-108">ImmutabilityPolicyObject</span></span>
```
Lock-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ce781-109">설명은</span><span class="sxs-lookup"><span data-stu-id="ce781-109">DESCRIPTION</span></span>
<span data-ttu-id="ce781-110">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet은 저장소 blob 컨테이너의 ImmutabilityPolicy를 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-110">The **Lock-AzureRmStorageContainerImmutabilityPolicy** cmdlet locks ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="ce781-111">예제의</span><span class="sxs-lookup"><span data-stu-id="ce781-111">EXAMPLES</span></span>

### <span data-ttu-id="ce781-112">예제 1: 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 잠그기</span><span class="sxs-lookup"><span data-stu-id="ce781-112">Example 1: Lock ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="ce781-113">이 명령은 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-113">This command Locks ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="ce781-114">예제 2: 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 잠그기</span><span class="sxs-lookup"><span data-stu-id="ce781-114">Example 2: Lock ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag -Force
```

<span data-ttu-id="ce781-115">이 명령을 사용 하면 저장소 blob 컨테이너의 ImmutabilityPolicy이 저장소 계정 개체와 함께 잠깁니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-115">This command locks ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="ce781-116">예제 3: 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너 ImmutabilityPolicyof 잠금</span><span class="sxs-lookup"><span data-stu-id="ce781-116">Example 3: Lock ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Lock-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag -Force
```

<span data-ttu-id="ce781-117">이 명령은 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-117">This command locks ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="ce781-118">예제 4: ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 잠그기</span><span class="sxs-lookup"><span data-stu-id="ce781-118">Example 4: Lock ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Lock-AzureRmStorageContainerImmutabilityPolicy -Force
```

<span data-ttu-id="ce781-119">이 명령은 ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 잠급니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-119">This command locks ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> 

## <span data-ttu-id="ce781-120">변수</span><span class="sxs-lookup"><span data-stu-id="ce781-120">PARAMETERS</span></span>

### <span data-ttu-id="ce781-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="ce781-121">-Container</span></span>
<span data-ttu-id="ce781-122">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="ce781-122">Storage container object</span></span>

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

### <span data-ttu-id="ce781-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="ce781-123">-ContainerName</span></span>
<span data-ttu-id="ce781-124">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="ce781-124">Container Name</span></span>

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

### <span data-ttu-id="ce781-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce781-125">-DefaultProfile</span></span>
<span data-ttu-id="ce781-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ce781-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="ce781-127">-Etag</span></span>
<span data-ttu-id="ce781-128">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="ce781-128">Immutability policy etag.</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ce781-129">-Force</span><span class="sxs-lookup"><span data-stu-id="ce781-129">-Force</span></span>
<span data-ttu-id="ce781-130">강제로 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-130">Force to remove the ImmutabilityPolicy.</span></span>

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

### <span data-ttu-id="ce781-131">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ce781-131">-InputObject</span></span>
<span data-ttu-id="ce781-132">제거할 ImmutabilityPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="ce781-132">ImmutabilityPolicy Object to Remove</span></span>

```yaml
Type: PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ce781-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce781-133">-ResourceGroupName</span></span>
<span data-ttu-id="ce781-134">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-134">Resource Group Name.</span></span>

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

### <span data-ttu-id="ce781-135">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="ce781-135">-StorageAccount</span></span>
<span data-ttu-id="ce781-136">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="ce781-136">Storage account object</span></span>

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

### <span data-ttu-id="ce781-137">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ce781-137">-StorageAccountName</span></span>
<span data-ttu-id="ce781-138">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-138">Storage Account Name.</span></span>

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

### <span data-ttu-id="ce781-139">-확인</span><span class="sxs-lookup"><span data-stu-id="ce781-139">-Confirm</span></span>
<span data-ttu-id="ce781-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ce781-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ce781-141">-WhatIf</span></span>
<span data-ttu-id="ce781-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ce781-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ce781-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce781-144">CommonParameters</span></span>
<span data-ttu-id="ce781-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce781-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ce781-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce781-147">입력</span><span class="sxs-lookup"><span data-stu-id="ce781-147">INPUTS</span></span>

### <span data-ttu-id="ce781-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ce781-148">System.String</span></span>
<span data-ttu-id="ce781-149">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ce781-150">출력</span><span class="sxs-lookup"><span data-stu-id="ce781-150">OUTPUTS</span></span>

### <span data-ttu-id="ce781-151">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="ce781-151">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="ce781-152">상속자</span><span class="sxs-lookup"><span data-stu-id="ce781-152">NOTES</span></span>

## <span data-ttu-id="ce781-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce781-153">RELATED LINKS</span></span>

