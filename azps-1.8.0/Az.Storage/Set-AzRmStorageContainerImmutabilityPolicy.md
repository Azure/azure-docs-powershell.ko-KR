---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.Management.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azrmstoragecontainerimmutabilitypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzRmStorageContainerImmutabilityPolicy.md
ms.openlocfilehash: c216765657cc87c958cc20dd0f2014f0e1c16970
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698551"
---
# <span data-ttu-id="50dbf-101">Set-AzRmStorageContainerImmutabilityPolicy</span><span class="sxs-lookup"><span data-stu-id="50dbf-101">Set-AzRmStorageContainerImmutabilityPolicy</span></span>

## <span data-ttu-id="50dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="50dbf-103">저장소 blob 컨테이너의 ImmutabilityPolicy를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-103">Creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="50dbf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="50dbf-104">SYNTAX</span></span>

### <span data-ttu-id="50dbf-105">AccountName (기본값)</span><span class="sxs-lookup"><span data-stu-id="50dbf-105">AccountName (Default)</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> [-Etag <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dbf-106">ExtendAccountName</span><span class="sxs-lookup"><span data-stu-id="50dbf-106">ExtendAccountName</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-ResourceGroupName] <String> [-StorageAccountName] <String>
 -ContainerName <String> -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dbf-107">AccountObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-107">AccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="50dbf-108">ExtendAccountObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-108">ExtendAccountObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -ContainerName <String> -StorageAccount <PSStorageAccount>
 -ImmutabilityPeriod <Int32> -Etag <String> [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dbf-109">ContainerObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-109">ContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32>
 [-Etag <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dbf-110">ExtendContainerObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-110">ExtendContainerObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy -Container <PSContainer> -ImmutabilityPeriod <Int32> -Etag <String>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dbf-111">ImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-111">ImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="50dbf-112">ExtendImmutabilityPolicyObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-112">ExtendImmutabilityPolicyObject</span></span>
```
Set-AzRmStorageContainerImmutabilityPolicy [-InputObject] <PSImmutabilityPolicy> -ImmutabilityPeriod <Int32>
 [-ExtendPolicy] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="50dbf-113">설명은</span><span class="sxs-lookup"><span data-stu-id="50dbf-113">DESCRIPTION</span></span>
<span data-ttu-id="50dbf-114">**AzRmStorageContainerImmutabilityPolicy** Cmdlet은 저장소 blob 컨테이너의 ImmutabilityPolicy를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-114">The **Set-AzRmStorageContainerImmutabilityPolicy** cmdlet creates or updates ImmutabilityPolicy of a Storage blob containers</span></span>

## <span data-ttu-id="50dbf-115">예제의</span><span class="sxs-lookup"><span data-stu-id="50dbf-115">EXAMPLES</span></span>

### <span data-ttu-id="50dbf-116">예제 1: 저장소 계정 이름과 컨테이너 이름이 있는 저장소 blob 컨테이너의 ImmutabilityPolicy 만들기 또는 업데이트</span><span class="sxs-lookup"><span data-stu-id="50dbf-116">Example 1: Create or update ImmutabilityPolicy of a Storage blob container with Storage account name and container name</span></span>
```
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" -ImmutabilityPeriod 10
```

<span data-ttu-id="50dbf-117">이 명령은 저장소 계정 이름과 컨테이너 이름을 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 만들거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-117">This command creates or updates ImmutabilityPolicy of a Storage blob container with Storage account name and container name.</span></span>

### <span data-ttu-id="50dbf-118">예제 2: 저장소 계정 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 확장</span><span class="sxs-lookup"><span data-stu-id="50dbf-118">Example 2: Extend ImmutabilityPolicy of a Storage blob container, with Storage account object</span></span>
```
PS C:\>$accountObject = Get-AzStorageAccount -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount"
PS C:\>$policy = Get-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer"
PS C:\>Set-AzRmStorageContainerImmutabilityPolicy -StorageAccount $accountObject -ContainerName "myContainer" -ImmutabilityPeriod 20 -Etag $policy.Etag -ExtendPolicy
```

<span data-ttu-id="50dbf-119">이 명령은 저장소 blob 컨테이너의 ImmutabilityPolicy를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-119">This command extend ImmutabilityPolicy of a Storage blob container, with Storage account object.</span></span> <span data-ttu-id="50dbf-120">ImmutabilityPolicy Extend는 ImmutabilityPolicy이 잠긴 후에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-120">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

### <span data-ttu-id="50dbf-121">예제 3: 저장소 blob 컨테이너 업데이트 ImmutabilityPolicyof</span><span class="sxs-lookup"><span data-stu-id="50dbf-121">Example 3: Update ImmutabilityPolicyof a Storage blob container</span></span>
```
PS C:\>$containerObject = Get-AzStorageContainer -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -Name "myContainer"
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 12
PS C:\>$policy = Set-AzRmStorageContainerImmutabilityPolicy -Container $containerObject -ImmutabilityPeriod 9 -Etag $policy.Etag
```

<span data-ttu-id="50dbf-122">이 명령은 저장소 컨테이너 개체 2 번으로 저장소 blob 컨테이너의 ImmutabilityPolicy를 업데이트 하 고, 먼저 etag 없이 12 일을 ImmutabilityPeriod 다음, etag를 사용 하 여 9 일간 ImmutabilityPeriod 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-122">This command updates ImmutabilityPolicy of a Storage blob container with Storage container object 2 times, first to ImmutabilityPeriod 12 days without etag, then to ImmutabilityPeriod 9 days with etag.</span></span>

### <span data-ttu-id="50dbf-123">예제 4: ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy 확장</span><span class="sxs-lookup"><span data-stu-id="50dbf-123">Example 4: Extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object</span></span>
```
PS C:\>Get-AzRmStorageContainerImmutabilityPolicy -ResourceGroupName "myResourceGroup" -AccountName "myStorageAccount" -ContainerName "myContainer" | Set-AzRmStorageContainerImmutabilityPolicy -ImmutabilityPeriod 15 -ExtendPolicy
```

<span data-ttu-id="50dbf-124">이 명령은 ImmutabilityPolicy 개체를 사용 하 여 저장소 blob 컨테이너의 ImmutabilityPolicy를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-124">This command extend ImmutabilityPolicy of a Storage blob container, with ImmutabilityPolicy object.</span></span> <span data-ttu-id="50dbf-125">ImmutabilityPolicy Extend는 ImmutabilityPolicy이 잠긴 후에만 실행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-125">Extend ImmutabilityPolicy can only run after ImmutabilityPolicy is locked.</span></span>

## <span data-ttu-id="50dbf-126">변수</span><span class="sxs-lookup"><span data-stu-id="50dbf-126">PARAMETERS</span></span>

### <span data-ttu-id="50dbf-127">-컨테이너</span><span class="sxs-lookup"><span data-stu-id="50dbf-127">-Container</span></span>
<span data-ttu-id="50dbf-128">저장소 컨테이너 개체</span><span class="sxs-lookup"><span data-stu-id="50dbf-128">Storage container object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSContainer
Parameter Sets: ContainerObject, ExtendContainerObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-129">-ContainerName</span><span class="sxs-lookup"><span data-stu-id="50dbf-129">-ContainerName</span></span>
<span data-ttu-id="50dbf-130">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="50dbf-130">Container Name</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName, AccountObject, ExtendAccountObject
Aliases: N

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50dbf-131">-DefaultProfile</span></span>
<span data-ttu-id="50dbf-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="50dbf-133">-Etag</span><span class="sxs-lookup"><span data-stu-id="50dbf-133">-Etag</span></span>
<span data-ttu-id="50dbf-134">불변성 정책 etag.</span><span class="sxs-lookup"><span data-stu-id="50dbf-134">Immutability policy etag.</span></span> <span data-ttu-id="50dbf-135">-ExtendPolicy가 지정 되지 않은 경우 Etag는 선택 사항입니다. 사용자 Etag가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-135">If -ExtendPolicy is not specified, Etag is optional; else Etag is required.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, AccountObject, ContainerObject
Aliases: IfMatch

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject
Aliases: IfMatch

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-136">-ExtendPolicy</span><span class="sxs-lookup"><span data-stu-id="50dbf-136">-ExtendPolicy</span></span>
<span data-ttu-id="50dbf-137">ExtendPolicy를 표시 하 여 기존 ImmutabilityPolicy를 확장 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-137">Indicate ExtendPolicy to Extend an existing ImmutabilityPolicy.</span></span>  <span data-ttu-id="50dbf-138">ImmutabilityPolicy이 잠긴 후에만 연장할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-138">After ImmutabilityPolicy is locked, it can only be extend.</span></span> 

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ExtendAccountName, ExtendAccountObject, ExtendContainerObject, ExtendImmutabilityPolicyObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-139">-ImmutabilityPeriod</span><span class="sxs-lookup"><span data-stu-id="50dbf-139">-ImmutabilityPeriod</span></span>
<span data-ttu-id="50dbf-140">일 단위로 만든 후의 불변성 기간.</span><span class="sxs-lookup"><span data-stu-id="50dbf-140">Immutability period since creation in days.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: ImmutabilityPeriodSinceCreationInDays

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-141">-InputObject</span><span class="sxs-lookup"><span data-stu-id="50dbf-141">-InputObject</span></span>
<span data-ttu-id="50dbf-142">컨테이너 이름</span><span class="sxs-lookup"><span data-stu-id="50dbf-142">Container Name</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy
Parameter Sets: ImmutabilityPolicyObject, ExtendImmutabilityPolicyObject
Aliases: ImmutabilityPolicy

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50dbf-143">-ResourceGroupName</span></span>
<span data-ttu-id="50dbf-144">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-144">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-145">-StorageAccount</span><span class="sxs-lookup"><span data-stu-id="50dbf-145">-StorageAccount</span></span>
<span data-ttu-id="50dbf-146">저장소 계정 개체</span><span class="sxs-lookup"><span data-stu-id="50dbf-146">Storage account object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount
Parameter Sets: AccountObject, ExtendAccountObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-147">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="50dbf-147">-StorageAccountName</span></span>
<span data-ttu-id="50dbf-148">저장소 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-148">Storage Account Name.</span></span>

```yaml
Type: System.String
Parameter Sets: AccountName, ExtendAccountName
Aliases: AccountName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-149">-확인</span><span class="sxs-lookup"><span data-stu-id="50dbf-149">-Confirm</span></span>
<span data-ttu-id="50dbf-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-150">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="50dbf-151">-WhatIf</span></span>
<span data-ttu-id="50dbf-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="50dbf-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-153">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50dbf-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50dbf-154">CommonParameters</span></span>
<span data-ttu-id="50dbf-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50dbf-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50dbf-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50dbf-157">입력</span><span class="sxs-lookup"><span data-stu-id="50dbf-157">INPUTS</span></span>

### <span data-ttu-id="50dbf-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="50dbf-158">System.String</span></span>

### <span data-ttu-id="50dbf-159">Microsoft. Azure.. i m a. 모델. PSStorageAccount</span><span class="sxs-lookup"><span data-stu-id="50dbf-159">Microsoft.Azure.Commands.Management.Storage.Models.PSStorageAccount</span></span>

### <span data-ttu-id="50dbf-160">Microsoft. m a. 모델. PSContainer</span><span class="sxs-lookup"><span data-stu-id="50dbf-160">Microsoft.Azure.Commands.Management.Storage.Models.PSContainer</span></span>

### <span data-ttu-id="50dbf-161">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-161">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="50dbf-162">출력</span><span class="sxs-lookup"><span data-stu-id="50dbf-162">OUTPUTS</span></span>

### <span data-ttu-id="50dbf-163">PSImmutabilityPolicy를 통해 관리 합니다.</span><span class="sxs-lookup"><span data-stu-id="50dbf-163">Microsoft.Azure.Commands.Management.Storage.Models.PSImmutabilityPolicy</span></span>

## <span data-ttu-id="50dbf-164">상속자</span><span class="sxs-lookup"><span data-stu-id="50dbf-164">NOTES</span></span>

## <span data-ttu-id="50dbf-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50dbf-165">RELATED LINKS</span></span>
