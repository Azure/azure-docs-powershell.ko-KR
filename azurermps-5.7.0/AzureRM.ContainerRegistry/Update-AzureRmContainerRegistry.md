---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistry.md
ms.openlocfilehash: 468c4cfac836ca986d6cfbfd06f35032cca5b6a0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531085"
---
# <span data-ttu-id="19dda-101">Update-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19dda-101">Update-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="19dda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19dda-102">SYNOPSIS</span></span>
<span data-ttu-id="19dda-103">컨테이너 레지스트리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-103">Updates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="19dda-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19dda-104">SYNTAX</span></span>

### <span data-ttu-id="19dda-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="19dda-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dda-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dda-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dda-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19dda-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dda-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dda-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="19dda-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19dda-110">ResourceIdParameterSet</span></span>
```
Update-AzureRmContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19dda-111">설명은</span><span class="sxs-lookup"><span data-stu-id="19dda-111">DESCRIPTION</span></span>
<span data-ttu-id="19dda-112">Update-AzureRmContainerRegistry cmdlet은 컨테이너 레지스트리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-112">The Update-AzureRmContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="19dda-113">예제의</span><span class="sxs-lookup"><span data-stu-id="19dda-113">EXAMPLES</span></span>

### <span data-ttu-id="19dda-114">예제 1: 지정 된 컨테이너 레지스트리에 관리자 사용자 사용</span><span class="sxs-lookup"><span data-stu-id="19dda-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="19dda-115">이 명령은 지정 된 컨테이너 레지스트리에 대 한 관리자 사용자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="19dda-116">예제 2: 지정 된 컨테이너 레지스트리에 사용 되는 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="19dda-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="19dda-117">이 명령은 지정 된 컨테이너 레지스트리를 설정 하 여 \` 동일한 구독에서 기존 저장소 계정 mystorageaccount를 사용 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="19dda-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="19dda-118">변수</span><span class="sxs-lookup"><span data-stu-id="19dda-118">PARAMETERS</span></span>

### <span data-ttu-id="19dda-119">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="19dda-119">-DisableAdminUser</span></span>
<span data-ttu-id="19dda-120">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-120">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-121">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="19dda-121">-EnableAdminUser</span></span>
<span data-ttu-id="19dda-122">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-122">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-123">-이름</span><span class="sxs-lookup"><span data-stu-id="19dda-123">-Name</span></span>
<span data-ttu-id="19dda-124">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-124">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19dda-125">-ResourceGroupName</span></span>
<span data-ttu-id="19dda-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-126">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="19dda-127">-StorageAccountName</span></span>
<span data-ttu-id="19dda-128">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-128">The name of an existing storage account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-129">태그</span><span class="sxs-lookup"><span data-stu-id="19dda-129">-Tag</span></span>
<span data-ttu-id="19dda-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-130">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="19dda-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="19dda-131">For example:</span></span>

<span data-ttu-id="19dda-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="19dda-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-133">-확인</span><span class="sxs-lookup"><span data-stu-id="19dda-133">-Confirm</span></span>
<span data-ttu-id="19dda-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19dda-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19dda-135">-WhatIf</span></span>
<span data-ttu-id="19dda-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="19dda-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19dda-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19dda-138">-DefaultProfile</span></span>
<span data-ttu-id="19dda-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="19dda-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="19dda-140">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19dda-140">-ResourceId</span></span>
<span data-ttu-id="19dda-141">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="19dda-141">The container registry resource id</span></span>

```yaml
Type: String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="19dda-142">-Sku</span></span>
<span data-ttu-id="19dda-143">컨테이너 레지스트리 SKU.</span><span class="sxs-lookup"><span data-stu-id="19dda-143">Container Registry SKU.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="19dda-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19dda-144">CommonParameters</span></span>
<span data-ttu-id="19dda-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19dda-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19dda-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19dda-147">입력</span><span class="sxs-lookup"><span data-stu-id="19dda-147">INPUTS</span></span>

### <span data-ttu-id="19dda-148">않아야</span><span class="sxs-lookup"><span data-stu-id="19dda-148">None</span></span>
<span data-ttu-id="19dda-149">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19dda-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="19dda-150">출력</span><span class="sxs-lookup"><span data-stu-id="19dda-150">OUTPUTS</span></span>

### <span data-ttu-id="19dda-151">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19dda-151">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="19dda-152">상속자</span><span class="sxs-lookup"><span data-stu-id="19dda-152">NOTES</span></span>

## <span data-ttu-id="19dda-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19dda-153">RELATED LINKS</span></span>

[<span data-ttu-id="19dda-154">새로운 AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19dda-154">New-AzureRmContainerRegistry</span></span>](New-AzureRmContainerRegistry.md)

[<span data-ttu-id="19dda-155">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19dda-155">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="19dda-156">제거-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="19dda-156">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

