---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: 232d767130b789f61d7e4e21fa0bc7c0737c58dc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528224"
---
# <span data-ttu-id="f74bf-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f74bf-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="f74bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f74bf-102">SYNOPSIS</span></span>
<span data-ttu-id="f74bf-103">컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f74bf-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f74bf-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f74bf-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f74bf-105">DESCRIPTION</span></span>
<span data-ttu-id="f74bf-106">**새 AzureRmContainerRegistry** cmdlet은 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-106">The **New-AzureRmContainerRegistry** cmdlet creates a container registry.</span></span>

## <span data-ttu-id="f74bf-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f74bf-107">EXAMPLES</span></span>

### <span data-ttu-id="f74bf-108">예제 1: 새 저장소 계정으로 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="f74bf-108">Example 1: Create a container registry with a new storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : myregistry154817
```

<span data-ttu-id="f74bf-109">이 명령은 리소스 그룹에 새 저장소 계정이 있는 컨테이너 레지스트리를 만듭니다 `MyResourceGroup` .</span><span class="sxs-lookup"><span data-stu-id="f74bf-109">This command creates a container registry with a new storage account in the resource group `MyResourceGroup`.</span></span>

### <span data-ttu-id="f74bf-110">예제 2: 관리자가 사용 하도록 설정 된 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="f74bf-110">Example 2: Create a container registry with admin user enabled.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : True
StorageAccountName : myregistry154817
```

<span data-ttu-id="f74bf-111">이 명령은 관리자 사용자가 설정 된 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="f74bf-112">예제 3: 기존 저장소 계정을 사용 하 여 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="f74bf-112">Example 3: Create a container registry with an existing storage account.</span></span>
```
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

Id                 : /subscriptions/3eb31d8d-2879-4706-89b4-4dc4047726c6/resourceGroups/MyResourceGroup/providers/Microsoft.ContainerRegistry/registries/MyRegistry
ResourceGroupName  : MyResourceGroup
Name               : MyRegistry
Type               : Microsoft.ContainerRegistry/registries
Location           : westus
Tags               : {}
SkuName            : Basic
SkuTier            : Basic
LoginServer        : myregistry.azurecr.io
CreationDate       : 4/13/2017 3:48:57 PM
ProvisioningState  : Succeeded
AdminUserEnabled   : False
StorageAccountName : mystorageaccount
```

<span data-ttu-id="f74bf-113">이 명령은 같은 구독에 기존 저장소 계정이 있는 컨테이너 레지스트리를 만듭니다 `mystorageaccount` .</span><span class="sxs-lookup"><span data-stu-id="f74bf-113">This command creates a container registry with an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="f74bf-114">변수</span><span class="sxs-lookup"><span data-stu-id="f74bf-114">PARAMETERS</span></span>

### <span data-ttu-id="f74bf-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="f74bf-115">-EnableAdminUser</span></span>
<span data-ttu-id="f74bf-116">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-117">-위치</span><span class="sxs-lookup"><span data-stu-id="f74bf-117">-Location</span></span>
<span data-ttu-id="f74bf-118">컨테이너 레지스트리 위치.</span><span class="sxs-lookup"><span data-stu-id="f74bf-118">Container Registry Location.</span></span>
<span data-ttu-id="f74bf-119">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-119">Default to the location of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-120">-이름</span><span class="sxs-lookup"><span data-stu-id="f74bf-120">-Name</span></span>
<span data-ttu-id="f74bf-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-121">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f74bf-122">-ResourceGroupName</span></span>
<span data-ttu-id="f74bf-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-123">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="f74bf-124">-Sku</span></span>
<span data-ttu-id="f74bf-125">컨테이너 레지스트리 SKU.</span><span class="sxs-lookup"><span data-stu-id="f74bf-125">Container Registry SKU.</span></span>
<span data-ttu-id="f74bf-126">허용 되는 값: Basic.</span><span class="sxs-lookup"><span data-stu-id="f74bf-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="f74bf-127">-StorageAccountName</span></span>
<span data-ttu-id="f74bf-128">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-128">The name of an existing storage account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-129">태그</span><span class="sxs-lookup"><span data-stu-id="f74bf-129">-Tag</span></span>
<span data-ttu-id="f74bf-130">컨테이너 레지스트리 태그. 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="f74bf-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="f74bf-131">For example:</span></span>

<span data-ttu-id="f74bf-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="f74bf-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f74bf-133">-Confirm</span></span>
<span data-ttu-id="f74bf-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f74bf-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f74bf-135">-WhatIf</span></span>
<span data-ttu-id="f74bf-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f74bf-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f74bf-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f74bf-138">-DefaultProfile</span></span>
<span data-ttu-id="f74bf-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-139">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f74bf-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f74bf-140">CommonParameters</span></span>
<span data-ttu-id="f74bf-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f74bf-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f74bf-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f74bf-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f74bf-143">입력</span><span class="sxs-lookup"><span data-stu-id="f74bf-143">INPUTS</span></span>

## <span data-ttu-id="f74bf-144">출력</span><span class="sxs-lookup"><span data-stu-id="f74bf-144">OUTPUTS</span></span>

### <span data-ttu-id="f74bf-145">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f74bf-145">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="f74bf-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f74bf-146">NOTES</span></span>

## <span data-ttu-id="f74bf-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f74bf-147">RELATED LINKS</span></span>

[<span data-ttu-id="f74bf-148">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f74bf-148">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="f74bf-149">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f74bf-149">Update-AzureRmContainerRegistry</span></span>](./Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="f74bf-150">제거-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f74bf-150">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
