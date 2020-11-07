---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainer.md
ms.openlocfilehash: 089451a0a0aae399a18296fbf4982724b35d432e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711305"
---
# <span data-ttu-id="24641-101">Remove-AzureRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="24641-101">Remove-AzureRmStorageContainer</span></span>

## <span data-ttu-id="24641-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24641-102">SYNOPSIS</span></span>
<span data-ttu-id="24641-103">저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-103">Removes a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="24641-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24641-104">SYNTAX</span></span>

### <span data-ttu-id="24641-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="24641-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24641-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="24641-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24641-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="24641-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24641-108">설명은</span><span class="sxs-lookup"><span data-stu-id="24641-108">DESCRIPTION</span></span>
<span data-ttu-id="24641-109">**AzureRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-109">The **Remove-AzureRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="24641-110">예제의</span><span class="sxs-lookup"><span data-stu-id="24641-110">EXAMPLES</span></span>

### <span data-ttu-id="24641-111">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="24641-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="24641-112">이 명령은 저장소 계정 이름과 컨테이너 이름을 가진 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="24641-113">예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="24641-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="24641-114">이 명령은 저장소 계정 개체와 컨테이너 이름을 가진 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="24641-115">예제 3: 파이프라인을 사용 하 여 저장소 계정에서 모든 저장소 blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="24641-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainer -Force
```

<span data-ttu-id="24641-116">이 명령은 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="24641-117">변수</span><span class="sxs-lookup"><span data-stu-id="24641-117">PARAMETERS</span></span>

### <span data-ttu-id="24641-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24641-118">-DefaultProfile</span></span>
<span data-ttu-id="24641-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24641-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="24641-120">-Force</span><span class="sxs-lookup"><span data-stu-id="24641-120">-Force</span></span>
<span data-ttu-id="24641-121">컨테이너 및 모든 콘텐츠를 강제로 제거</span><span class="sxs-lookup"><span data-stu-id="24641-121">Force to remove the container and all content in it</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24641-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="24641-122">-InputObject</span></span>
<span data-ttu-id="24641-123">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="24641-123">Storage container object</span></span>

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

### <span data-ttu-id="24641-124">-이름</span><span class="sxs-lookup"><span data-stu-id="24641-124">-Name</span></span>
<span data-ttu-id="24641-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="24641-125">Container Name</span></span>

```yaml
Type: String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="24641-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24641-126">-PassThru</span></span>
<span data-ttu-id="24641-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="24641-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="24641-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24641-128">-ResourceGroupName</span></span>
<span data-ttu-id="24641-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24641-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="24641-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="24641-130">-StorageAccount</span></span>
<span data-ttu-id="24641-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="24641-131">Storage account object</span></span>

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

### <span data-ttu-id="24641-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="24641-132">-StorageAccountName</span></span>
<span data-ttu-id="24641-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24641-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="24641-134">-확인</span><span class="sxs-lookup"><span data-stu-id="24641-134">-Confirm</span></span>
<span data-ttu-id="24641-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24641-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24641-136">-WhatIf</span></span>
<span data-ttu-id="24641-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24641-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="24641-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24641-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="24641-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24641-139">CommonParameters</span></span>
<span data-ttu-id="24641-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24641-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24641-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24641-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24641-142">입력</span><span class="sxs-lookup"><span data-stu-id="24641-142">INPUTS</span></span>

### <span data-ttu-id="24641-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24641-143">System.String</span></span>

## <span data-ttu-id="24641-144">출력</span><span class="sxs-lookup"><span data-stu-id="24641-144">OUTPUTS</span></span>

### <span data-ttu-id="24641-145">System. 개체</span><span class="sxs-lookup"><span data-stu-id="24641-145">System.Object</span></span>

## <span data-ttu-id="24641-146">상속자</span><span class="sxs-lookup"><span data-stu-id="24641-146">NOTES</span></span>

## <span data-ttu-id="24641-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24641-147">RELATED LINKS</span></span>
