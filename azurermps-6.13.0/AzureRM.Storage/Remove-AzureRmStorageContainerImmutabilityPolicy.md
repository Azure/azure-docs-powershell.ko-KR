---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: 74963ef36a33bed6145d315f5792aa776a36bc7d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531319"
---
# <span data-ttu-id="02a62-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="02a62-101">Remove-AzureRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="02a62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02a62-102">SYNOPSIS</span></span>
<span data-ttu-id="02a62-103">저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-103">Removes ImmutabilityPolicy of a Storage blob containers</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02a62-104">구문과</span><span class="sxs-lookup"><span data-stu-id="02a62-104">SYNTAX</span></span>

### <span data-ttu-id="02a62-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="02a62-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 [-ContainerName] <String> [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="02a62-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="02a62-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy [-ContainerName] <String> -StorageAccount <PSStorageAccount>
 [-Etag] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a62-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="02a62-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -Container <PSContainer> [-Etag] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02a62-108">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="02a62-108">ImmutabilityPolicyObject</span></span>
```
Remove-AzureRmStorageContainerImmutabilityPolicy -InputObject <PSImmutabilityPolicy>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02a62-109">설명은</span><span class="sxs-lookup"><span data-stu-id="02a62-109">DESCRIPTION</span></span>
<span data-ttu-id="02a62-110">**AzureRmStorageContainerImmutabilityPolicy** Cmdlet은 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-110">The **Remove-AzureRmStorageContainerImmutabilityPolicy** cmdlet removes ImmutabilityPolicy of a Storage blob containers.</span></span>

## <span data-ttu-id="02a62-111">예제의</span><span class="sxs-lookup"><span data-stu-id="02a62-111">EXAMPLES</span></span>

### <span data-ttu-id="02a62-112">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="02a62-112">Example 1: Remove ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="02a62-113">이 명령은 저장소 계정 이름과 컨테이너 이름을 가진 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-113">This command removes ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="02a62-114">예제 2: 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="02a62-114">Example 2: Remove ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -Etag $policy.Etag
```

<span data-ttu-id="02a62-115">이 명령은 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-115">This command removes ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> 

### <span data-ttu-id="02a62-116">예제 3: 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너 ImmutabilityPolicyof 제거</span><span class="sxs-lookup"><span data-stu-id="02a62-116">Example 3: Remove ImmutabilityPolicyof a Storage blob container, with container object</span></span>
```
PS C:\>$containerObject = Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Get-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject
PS C:\>Remove-AzureRmStorageContainerImmutabilityPolicy -Container $containerObject -Etag $policy.Etag
```

<span data-ttu-id="02a62-117">이 명령은 저장소 컨테이너 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-117">This command removes ImmutabilityPolicy of a Storage blob container with Storage container object.</span></span>

### <span data-ttu-id="02a62-118">예제 4: ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 제거</span><span class="sxs-lookup"><span data-stu-id="02a62-118">Example 4: Remove ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzureRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Remove-AzureRmStorageContainerImmutabilityPolicy
```

<span data-ttu-id="02a62-119">이 명령은 ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-119">This command removes ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span>

## <span data-ttu-id="02a62-120">변수</span><span class="sxs-lookup"><span data-stu-id="02a62-120">PARAMETERS</span></span>

### <span data-ttu-id="02a62-121">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="02a62-121">-Container</span></span>
<span data-ttu-id="02a62-122">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="02a62-122">Storage container object</span></span>

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

### <span data-ttu-id="02a62-123">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="02a62-123">-ContainerName</span></span>
<span data-ttu-id="02a62-124">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="02a62-124">Container Name</span></span>

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

### <span data-ttu-id="02a62-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02a62-125">-DefaultProfile</span></span>
<span data-ttu-id="02a62-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="02a62-127">-Etag</span><span class="sxs-lookup"><span data-stu-id="02a62-127">-Etag</span></span>
<span data-ttu-id="02a62-128">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="02a62-128">Immutability policy etag.</span></span>

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

### <span data-ttu-id="02a62-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02a62-129">-InputObject</span></span>
<span data-ttu-id="02a62-130">제거할 ImmutabilityPolicy 개체</span><span class="sxs-lookup"><span data-stu-id="02a62-130">ImmutabilityPolicy Object to Remove</span></span>

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

### <span data-ttu-id="02a62-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02a62-131">-ResourceGroupName</span></span>
<span data-ttu-id="02a62-132">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-132">Resource Group Name.</span></span>

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

### <span data-ttu-id="02a62-133">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="02a62-133">-StorageAccount</span></span>
<span data-ttu-id="02a62-134">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="02a62-134">Storage account object</span></span>

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

### <span data-ttu-id="02a62-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="02a62-135">-StorageAccountName</span></span>
<span data-ttu-id="02a62-136">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-136">Storage Account Name.</span></span>

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

### <span data-ttu-id="02a62-137">-확인</span><span class="sxs-lookup"><span data-stu-id="02a62-137">-Confirm</span></span>
<span data-ttu-id="02a62-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02a62-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02a62-139">-WhatIf</span></span>
<span data-ttu-id="02a62-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02a62-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02a62-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02a62-142">CommonParameters</span></span>
<span data-ttu-id="02a62-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02a62-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02a62-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02a62-145">입력</span><span class="sxs-lookup"><span data-stu-id="02a62-145">INPUTS</span></span>

### <span data-ttu-id="02a62-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02a62-146">System.String</span></span>
<span data-ttu-id="02a62-147">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-147">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="02a62-148">출력</span><span class="sxs-lookup"><span data-stu-id="02a62-148">OUTPUTS</span></span>

### <span data-ttu-id="02a62-149">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="02a62-149">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="02a62-150">상속자</span><span class="sxs-lookup"><span data-stu-id="02a62-150">NOTES</span></span>

## <span data-ttu-id="02a62-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02a62-151">RELATED LINKS</span></span>

