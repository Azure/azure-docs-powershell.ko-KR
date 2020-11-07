---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/remove-azrmstoragecontainer
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Remove-AzRmStorageContainer.md
ms.openlocfilehash: d7a4563a32da28215dbb9b6dab2b911a500183a9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93874253"
---
# <span data-ttu-id="f47ef-101">Remove-AzRmStorageContainer</span><span class="sxs-lookup"><span data-stu-id="f47ef-101">Remove-AzRmStorageContainer</span></span>

## <span data-ttu-id="f47ef-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f47ef-102">SYNOPSIS</span></span>
<span data-ttu-id="f47ef-103">저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-103">Removes a Storage blob container</span></span>

## <span data-ttu-id="f47ef-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f47ef-104">SYNTAX</span></span>

### <span data-ttu-id="f47ef-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f47ef-105">AccountName (Default)</span></span>
```
Remove-AzRmStorageContainer [-ResourceGroupName] <String> [-StorageAccountName] <String> -Name <String>
 [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f47ef-106">AccountObject</span><span class="sxs-lookup"><span data-stu-id="f47ef-106">AccountObject</span></span>
```
Remove-AzRmStorageContainer -Name <String> -StorageAccount <PSStorageAccount> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f47ef-107">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="f47ef-107">ContainerObject</span></span>
```
Remove-AzRmStorageContainer -InputObject <PSContainer> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f47ef-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f47ef-108">DESCRIPTION</span></span>
<span data-ttu-id="f47ef-109">**AzRmStorageContainer** Cmdlet은 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-109">The **Remove-AzRmStorageContainer** cmdlet removes a Storage blob container</span></span>

## <span data-ttu-id="f47ef-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f47ef-110">EXAMPLES</span></span>

### <span data-ttu-id="f47ef-111">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="f47ef-111">Example 1: Remove a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Remove-AzRmStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer"
```

<span data-ttu-id="f47ef-112">이 명령은 저장소 계정 이름과 컨테이너 이름을 가진 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-112">This command removes a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="f47ef-113">예제 2: 저장소 계정 개체 및 컨테이너 이름이 있는 저장소 blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="f47ef-113">Example 2: Remove a Storage blob container with Storage account object and container name</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>Remove-AzRmStorageContainer -StorageAccount $accountObject -ContainerName "myContainer"
```

<span data-ttu-id="f47ef-114">이 명령은 저장소 계정 개체와 컨테이너 이름을 가진 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-114">This command removes a Storage blob container with Storage account object and container name.</span></span>

### <span data-ttu-id="f47ef-115">예제 3: 파이프라인을 사용 하 여 저장소 계정에서 모든 저장소 blob 컨테이너 제거</span><span class="sxs-lookup"><span data-stu-id="f47ef-115">Example 3: Remove all Storage blob containers in a Storage account with pipeline</span></span>
```
PS C:\>Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" | Remove-AzRmStorageContainer -Force
```

<span data-ttu-id="f47ef-116">이 명령은 파이프라인을 사용 하 여 저장소 계정에 있는 모든 저장소 blob 컨테이너를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-116">This command removes all Storage blob containers in a Storage account with pipeline.</span></span>

## <span data-ttu-id="f47ef-117">변수</span><span class="sxs-lookup"><span data-stu-id="f47ef-117">PARAMETERS</span></span>

### <span data-ttu-id="f47ef-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f47ef-118">-DefaultProfile</span></span>
<span data-ttu-id="f47ef-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f47ef-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f47ef-120">-Force</span></span>
<span data-ttu-id="f47ef-121">컨테이너 및 모든 콘텐츠를 강제로 제거</span><span class="sxs-lookup"><span data-stu-id="f47ef-121">Force to remove the container and all content in it</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47ef-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f47ef-122">-InputObject</span></span>
<span data-ttu-id="f47ef-123">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="f47ef-123">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject
Aliases: Container

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f47ef-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f47ef-124">-Name</span></span>
<span data-ttu-id="f47ef-125">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="f47ef-125">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject
Aliases: N, ContainerName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f47ef-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f47ef-126">-PassThru</span></span>
<span data-ttu-id="f47ef-127">{{Fill PassThru 설명}}</span><span class="sxs-lookup"><span data-stu-id="f47ef-127">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f47ef-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f47ef-128">-ResourceGroupName</span></span>
<span data-ttu-id="f47ef-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-129">Resource Group Name.</span></span>

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

### <span data-ttu-id="f47ef-130">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="f47ef-130">-StorageAccount</span></span>
<span data-ttu-id="f47ef-131">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="f47ef-131">Storage account object</span></span>

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

### <span data-ttu-id="f47ef-132">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f47ef-132">-StorageAccountName</span></span>
<span data-ttu-id="f47ef-133">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-133">Storage Account Name.</span></span>

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

### <span data-ttu-id="f47ef-134">-확인</span><span class="sxs-lookup"><span data-stu-id="f47ef-134">-Confirm</span></span>
<span data-ttu-id="f47ef-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47ef-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f47ef-136">-WhatIf</span></span>
<span data-ttu-id="f47ef-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f47ef-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-138">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f47ef-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f47ef-139">CommonParameters</span></span>
<span data-ttu-id="f47ef-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f47ef-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f47ef-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f47ef-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f47ef-142">입력</span><span class="sxs-lookup"><span data-stu-id="f47ef-142">INPUTS</span></span>

### <span data-ttu-id="f47ef-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f47ef-143">System.String</span></span>

### <span data-ttu-id="f47ef-144">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="f47ef-144">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="f47ef-145">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="f47ef-145">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

## <span data-ttu-id="f47ef-146">출력</span><span class="sxs-lookup"><span data-stu-id="f47ef-146">OUTPUTS</span></span>

### <span data-ttu-id="f47ef-147">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f47ef-147">System.Boolean</span></span>

## <span data-ttu-id="f47ef-148">상속자</span><span class="sxs-lookup"><span data-stu-id="f47ef-148">NOTES</span></span>

## <span data-ttu-id="f47ef-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f47ef-149">RELATED LINKS</span></span>
