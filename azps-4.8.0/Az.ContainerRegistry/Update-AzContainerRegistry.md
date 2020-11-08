---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistry.md
ms.openlocfilehash: 606f92a3cc75deb40b3781b3578e38794ae65b2b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049079"
---
# <span data-ttu-id="b4983-101">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4983-101">Update-AzContainerRegistry</span></span>

## <span data-ttu-id="b4983-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4983-102">SYNOPSIS</span></span>
<span data-ttu-id="b4983-103">컨테이너 레지스트리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-103">Updates a container registry.</span></span>

## <span data-ttu-id="b4983-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b4983-104">SYNTAX</span></span>

### <span data-ttu-id="b4983-105">NameResourceGroupParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="b4983-105">NameResourceGroupParameterSet (Default)</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4983-106">EnableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4983-106">EnableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-EnableAdminUser] [-Tag <Hashtable>]
 [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4983-107">DisableAdminUserByResourceNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4983-107">DisableAdminUserByResourceNameParameterSet</span></span>
```
Update-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-DisableAdminUser]
 [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4983-108">EnableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4983-108">EnableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b4983-109">DisableAdminUserByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4983-109">DisableAdminUserByResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-DisableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-Sku <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b4983-110">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="b4983-110">ResourceIdParameterSet</span></span>
```
Update-AzContainerRegistry [-Tag <Hashtable>] [-StorageAccountName <String>] [-Sku <String>]
 -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4983-111">설명은</span><span class="sxs-lookup"><span data-stu-id="b4983-111">DESCRIPTION</span></span>
<span data-ttu-id="b4983-112">Update-AzContainerRegistry cmdlet은 컨테이너 레지스트리를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-112">The Update-AzContainerRegistry cmdlet updates a container registry.</span></span>

## <span data-ttu-id="b4983-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b4983-113">EXAMPLES</span></span>

### <span data-ttu-id="b4983-114">예제 1: 지정 된 컨테이너 레지스트리에 관리자 사용자 사용</span><span class="sxs-lookup"><span data-stu-id="b4983-114">Example 1: Enable admin user for a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -EnableAdminUser

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True
```

<span data-ttu-id="b4983-115">이 명령은 지정 된 컨테이너 레지스트리에 대 한 관리자 사용자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-115">This command enables admin user for the specified container registry.</span></span>

### <span data-ttu-id="b4983-116">예제 2: 지정 된 컨테이너 레지스트리에 사용 되는 저장소 계정 설정</span><span class="sxs-lookup"><span data-stu-id="b4983-116">Example 2: Set the storage account used by a specified container registry</span></span>
```powershell
PS C:\>Update-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name        Sku        LoginServer                    CreationDate         Provisioni AdminUserE StorageAccountName
                                                                                    ngState    nabled
-------------        ---        -----------                    ------------         ---------- ---------- ------------------
MyRegistry           Basic      myregistry.azurecr.io          11/20/2017 10:05:... Succeeded  True       mystorageaccount
```

<span data-ttu-id="b4983-117">이 명령은 지정 된 컨테이너 레지스트리를 설정 하 여 \` 동일한 구독에서 기존 저장소 계정 mystorageaccount를 사용 합니다 \` .</span><span class="sxs-lookup"><span data-stu-id="b4983-117">This command sets the specified container registry to use an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="b4983-118">변수</span><span class="sxs-lookup"><span data-stu-id="b4983-118">PARAMETERS</span></span>

### <span data-ttu-id="b4983-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4983-119">-DefaultProfile</span></span>
<span data-ttu-id="b4983-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b4983-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b4983-121">-DisableAdminUser</span><span class="sxs-lookup"><span data-stu-id="b4983-121">-DisableAdminUser</span></span>
<span data-ttu-id="b4983-122">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-122">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: DisableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceIdParameterSet
Aliases: DisableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4983-123">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="b4983-123">-EnableAdminUser</span></span>
<span data-ttu-id="b4983-124">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-124">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: EnableAdminUserByResourceNameParameterSet, EnableAdminUserByResourceIdParameterSet
Aliases: EnableAdmin

Required: True
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4983-125">-이름</span><span class="sxs-lookup"><span data-stu-id="b4983-125">-Name</span></span>
<span data-ttu-id="b4983-126">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-126">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4983-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b4983-127">-ResourceGroupName</span></span>
<span data-ttu-id="b4983-128">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-128">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceNameParameterSet, DisableAdminUserByResourceNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4983-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b4983-129">-ResourceId</span></span>
<span data-ttu-id="b4983-130">컨테이너 레지스트리 리소스 id</span><span class="sxs-lookup"><span data-stu-id="b4983-130">The container registry resource id</span></span>

```yaml
Type: System.String
Parameter Sets: EnableAdminUserByResourceIdParameterSet, DisableAdminUserByResourceIdParameterSet, ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b4983-131">-Sku</span><span class="sxs-lookup"><span data-stu-id="b4983-131">-Sku</span></span>
<span data-ttu-id="b4983-132">컨테이너 레지스트리 SKU.</span><span class="sxs-lookup"><span data-stu-id="b4983-132">Container Registry SKU.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Classic, Basic, Premium, Standard

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b4983-133">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="b4983-133">-StorageAccountName</span></span>
<span data-ttu-id="b4983-134">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-134">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="b4983-135">태그</span><span class="sxs-lookup"><span data-stu-id="b4983-135">-Tag</span></span>
<span data-ttu-id="b4983-136">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-136">Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="b4983-137">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b4983-137">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b4983-138">-확인</span><span class="sxs-lookup"><span data-stu-id="b4983-138">-Confirm</span></span>
<span data-ttu-id="b4983-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4983-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4983-140">-WhatIf</span></span>
<span data-ttu-id="b4983-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b4983-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4983-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4983-143">CommonParameters</span></span>
<span data-ttu-id="b4983-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b4983-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4983-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b4983-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b4983-146">입력</span><span class="sxs-lookup"><span data-stu-id="b4983-146">INPUTS</span></span>

### <span data-ttu-id="b4983-147">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b4983-147">System.String</span></span>

## <span data-ttu-id="b4983-148">출력</span><span class="sxs-lookup"><span data-stu-id="b4983-148">OUTPUTS</span></span>

### <span data-ttu-id="b4983-149">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4983-149">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="b4983-150">상속자</span><span class="sxs-lookup"><span data-stu-id="b4983-150">NOTES</span></span>

## <span data-ttu-id="b4983-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b4983-151">RELATED LINKS</span></span>

[<span data-ttu-id="b4983-152">새로운 AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4983-152">New-AzContainerRegistry</span></span>](New-AzContainerRegistry.md)

[<span data-ttu-id="b4983-153">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4983-153">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="b4983-154">제거-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="b4983-154">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

