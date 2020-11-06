---
external help file: Microsoft.Azure.Commands.Management.Storage.dll-Help.xml
Module Name: AzureRM.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.storage/remove-azurermstoragecontainerlegalhold
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Storage/Commands.Management.Storage/help/Remove-AzureRmStorageContainerLegalHold.md
ms.openlocfilehash: da0793e7eb10f7b83d785aea34866842abe9b887
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531318"
---
# <span data-ttu-id="fcce7-101">Remove-AzureRmStorageContainerLegalHold</span><span class="sxs-lookup"><span data-stu-id="fcce7-101">Remove-AzureRmStorageContainerLegalHold</span></span>

## <span data-ttu-id="fcce7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fcce7-102">SYNOPSIS</span></span>
<span data-ttu-id="fcce7-103">저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-103">Removes legal hold tags from a Storage blob container</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fcce7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fcce7-104">SYNTAX</span></span>

### <span data-ttu-id="fcce7-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="fcce7-105">AccountName (Default)</span></span>
```
Remove-AzureRmStorageContainerLegalHold [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -Name <String> -Tag <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fcce7-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="fcce7-106">AccountObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Name <String> -StorageAccount <PSStorageAccount> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fcce7-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="fcce7-107">ContainerObject</span></span>
```
Remove-AzureRmStorageContainerLegalHold -Container <PSContainer> -Tag <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fcce7-108">설명은</span><span class="sxs-lookup"><span data-stu-id="fcce7-108">DESCRIPTION</span></span>
<span data-ttu-id="fcce7-109">**AzureRmStorageContainerLegalHold** Cmdlet은 저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-109">The **Remove-AzureRmStorageContainerLegalHold** cmdlet removes legal hold tags from a Storage blob container</span></span>

## <span data-ttu-id="fcce7-110">예제의</span><span class="sxs-lookup"><span data-stu-id="fcce7-110">EXAMPLES</span></span>

### <span data-ttu-id="fcce7-111">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너에서 법률 보존 태그 제거</span><span class="sxs-lookup"><span data-stu-id="fcce7-111">Example 1: Remove legal hold tags from a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzureRmStorageContainerLegalHold -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -Tag  tag1
```

<span data-ttu-id="fcce7-112">이 명령은 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-112">This command removes legal hold tags from a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="fcce7-113">예제 2: 저장소 계정 개체 및 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 법률 보존 태그 제거</span><span class="sxs-lookup"><span data-stu-id="fcce7-113">Example 2: Remove legal hold tags from a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzureRmStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzureRmStorageContainerLegalHold -StorageAccount $accountObject -ContainerName "myContainer"  -Tag  tag1,tag2 
```

<span data-ttu-id="fcce7-114">이 명령은 저장소 계정 개체와 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너에서 보존 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-114">This command removes legal hold tags from a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="fcce7-115">예제 3: 파이프라인을 사용 하 여 저장소 계정의 모든 저장소 blob 컨테이너에서 올바른 보류 태그 제거</span><span class="sxs-lookup"><span data-stu-id="fcce7-115">Example 3: Remove legal hold tags from all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzureRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzureRmStorageContainerLegalHold -Tag  tag1
```

<span data-ttu-id="fcce7-116">이 명령은 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너에서 유지 되는 legal 태그를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-116">This command removes legal hold tags from all Storage blob containers in a Storage account with pipeline.</span></span>


## <span data-ttu-id="fcce7-117">변수</span><span class="sxs-lookup"><span data-stu-id="fcce7-117">PARAMETERS</span></span>

### <span data-ttu-id="fcce7-118">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="fcce7-118">-Container</span></span>
<span data-ttu-id="fcce7-119">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="fcce7-119">Storage container object</span></span>

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

### <span data-ttu-id="fcce7-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fcce7-120">-DefaultProfile</span></span>
<span data-ttu-id="fcce7-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fcce7-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fcce7-122">-Name</span></span>
<span data-ttu-id="fcce7-123">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="fcce7-123">Container Name</span></span>

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

### <span data-ttu-id="fcce7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fcce7-124">-ResourceGroupName</span></span>
<span data-ttu-id="fcce7-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="fcce7-126">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="fcce7-126">-StorageAccount</span></span>
<span data-ttu-id="fcce7-127">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="fcce7-127">Storage account object</span></span>

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

### <span data-ttu-id="fcce7-128">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="fcce7-128">-StorageAccountName</span></span>
<span data-ttu-id="fcce7-129">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-129">Storage Account Name.</span></span>

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

### <span data-ttu-id="fcce7-130">태그</span><span class="sxs-lookup"><span data-stu-id="fcce7-130">-Tag</span></span>
<span data-ttu-id="fcce7-131">컨테이너 LegalHold 태그</span><span class="sxs-lookup"><span data-stu-id="fcce7-131">Container LegalHold Tags</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fcce7-132">-확인</span><span class="sxs-lookup"><span data-stu-id="fcce7-132">-Confirm</span></span>
<span data-ttu-id="fcce7-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fcce7-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fcce7-134">-WhatIf</span></span>
<span data-ttu-id="fcce7-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fcce7-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fcce7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fcce7-137">CommonParameters</span></span>
<span data-ttu-id="fcce7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fcce7-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fcce7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fcce7-140">입력</span><span class="sxs-lookup"><span data-stu-id="fcce7-140">INPUTS</span></span>

### <span data-ttu-id="fcce7-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fcce7-141">System.String</span></span>

## <span data-ttu-id="fcce7-142">출력</span><span class="sxs-lookup"><span data-stu-id="fcce7-142">OUTPUTS</span></span>

### <span data-ttu-id="fcce7-143">PSLegalHold를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="fcce7-143">Microsoft.Azure.Commands.Management.Storage.Models.PSLegalHold</span></span>

## <span data-ttu-id="fcce7-144">상속자</span><span class="sxs-lookup"><span data-stu-id="fcce7-144">NOTES</span></span>

## <span data-ttu-id="fcce7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fcce7-145">RELATED LINKS</span></span>

