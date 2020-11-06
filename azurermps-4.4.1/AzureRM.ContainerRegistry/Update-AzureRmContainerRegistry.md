---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 5f59ae54d472d1d831b41f58789625c195961de5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535476"
---
# <span data-ttu-id="ae78a-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae78a-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="ae78a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae78a-102">SYNOPSIS</span></span>
<span data-ttu-id="ae78a-103">컨테이너 레지스트리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ae78a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ae78a-104">SYNTAX</span></span>

### <span data-ttu-id="ae78a-105">비어 있음 (기본값)</span><span class="sxs-lookup"><span data-stu-id="ae78a-105">Empty (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="ae78a-106">EnableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae78a-106">EnableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ae78a-107">DisableAdminUserParameterSet</span><span class="sxs-lookup"><span data-stu-id="ae78a-107">DisableAdminUserParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ae78a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="ae78a-108">DESCRIPTION</span></span>
<span data-ttu-id="ae78a-109">**업데이트 AzureRmContainerRegistry** cmdlet은 컨테이너 레지스트리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-109">The **Update-AzureRmContainerRegistry** cmdlet updates a container registry.</span></span>

## <span data-ttu-id="ae78a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ae78a-110">EXAMPLES</span></span>

### <span data-ttu-id="ae78a-111">예제 1: 지정 된 컨테이너 레지스트리에 관리자 사용자 사용</span><span class="sxs-lookup"><span data-stu-id="ae78a-111">Example 1: Enable admin user for a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

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

<span data-ttu-id="ae78a-112">이 명령은 지정 된 컨테이너 레지스트리에 대 한 관리자 사용자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-112">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="ae78a-113">예제 2: 지정 된 컨테이너 레지스트리에 사용 되는 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="ae78a-113">Example 2: Set the storage account used by a specified container registry</span></span>
```
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

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
StorageAccountName : mystorageaccount
```

<span data-ttu-id="ae78a-114">이 명령은 지정 된 컨테이너 레지스트리가 동일한 구독에서 기존 저장소 계정을 사용 하도록 설정 합니다 `mystorageaccount` .</span><span class="sxs-lookup"><span data-stu-id="ae78a-114">This command sets the specified container registry to use an existing storage account `mystorageaccount` in the same subscription.</span></span>

## <span data-ttu-id="ae78a-115">변수</span><span class="sxs-lookup"><span data-stu-id="ae78a-115">PARAMETERS</span></span>

### <span data-ttu-id="ae78a-116">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ae78a-116">-DisableAdminUser</span></span>
<span data-ttu-id="ae78a-117">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-117">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: DisableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae78a-118">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="ae78a-118">-EnableAdminUser</span></span>
<span data-ttu-id="ae78a-119">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-119">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserParameterSet
Aliases: EnableAdmin

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ae78a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="ae78a-120">-Name</span></span>
<span data-ttu-id="ae78a-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="ae78a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ae78a-122">-ResourceGroupName</span></span>
<span data-ttu-id="ae78a-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="ae78a-124">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="ae78a-124">-StorageAccountName</span></span>
<span data-ttu-id="ae78a-125">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-125">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="ae78a-126">태그</span><span class="sxs-lookup"><span data-stu-id="ae78a-126">-Tag</span></span>
<span data-ttu-id="ae78a-127">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-127">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="ae78a-128">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="ae78a-128">For example:</span></span>

<span data-ttu-id="ae78a-129">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="ae78a-129">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="ae78a-130">-확인</span><span class="sxs-lookup"><span data-stu-id="ae78a-130">-Confirm</span></span>
<span data-ttu-id="ae78a-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ae78a-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ae78a-132">-WhatIf</span></span>
<span data-ttu-id="ae78a-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ae78a-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ae78a-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae78a-135">-DefaultProfile</span></span>
<span data-ttu-id="ae78a-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ae78a-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae78a-137">CommonParameters</span></span>
<span data-ttu-id="ae78a-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ae78a-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae78a-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ae78a-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae78a-140">입력</span><span class="sxs-lookup"><span data-stu-id="ae78a-140">INPUTS</span></span>

## <span data-ttu-id="ae78a-141">출력</span><span class="sxs-lookup"><span data-stu-id="ae78a-141">OUTPUTS</span></span>

### <span data-ttu-id="ae78a-142">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae78a-142">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="ae78a-143">상속자</span><span class="sxs-lookup"><span data-stu-id="ae78a-143">NOTES</span></span>

## <span data-ttu-id="ae78a-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae78a-144">RELATED LINKS</span></span>

[<span data-ttu-id="ae78a-145">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae78a-145">New-AzureRmContainerRegistry</span></span>](./New-AzureRmContainerRegistry.md)

[<span data-ttu-id="ae78a-146">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae78a-146">Get-AzureRmContainerRegistry</span></span>](./Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="ae78a-147">제거-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="ae78a-147">Remove-AzureRmContainerRegistry</span></span>](./Remove-AzureRmContainerRegistry.md)
