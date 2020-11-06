---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistry.md
ms.openlocfilehash: ce72af78fec87182e1061259cd0c0d51d9819767
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526903"
---
# <span data-ttu-id="82a8f-101">New-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82a8f-101">New-AzureRmContainerRegistry</span></span>

## <span data-ttu-id="82a8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82a8f-102">SYNOPSIS</span></span>
<span data-ttu-id="82a8f-103">컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-103">Creates a container registry.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="82a8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82a8f-104">SYNTAX</span></span>

```
New-AzureRmContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String>
 [-Location <String>] [-EnableAdminUser] [-Tag <Hashtable>] [-StorageAccountName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="82a8f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82a8f-105">DESCRIPTION</span></span>
<span data-ttu-id="82a8f-106">New-AzureRmContainerRegistry cmdlet은 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-106">The New-AzureRmContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="82a8f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="82a8f-107">EXAMPLES</span></span>

### <span data-ttu-id="82a8f-108">예제 1: 새 저장소 계정으로 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="82a8f-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="82a8f-109">이 명령은 리소스 그룹 myresourcegroup에 새 저장소 계정이 있는 컨테이너 레지스트리를 만듭니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="82a8f-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="82a8f-110">예제 2: 관리자가 사용 하도록 설정 된 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="82a8f-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="82a8f-111">이 명령은 관리자 사용자가 설정 된 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-111">This command creates a container registry with admin user enabled.</span></span>

### <span data-ttu-id="82a8f-112">예제 3: 기존 저장소 계정을 사용 하 여 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="82a8f-112">Example 3: Create a container registry with an existing storage account.</span></span>
```powershell
PS C:\>New-AzureRmContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -StorageAccountName "mystorageaccount"

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="82a8f-113">이 명령은 같은 구독에 기존 저장소 계정 mystorageaccount를 사용 하 여 컨테이너 레지스트리를 만듭니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="82a8f-113">This command creates a container registry with an existing storage account \`mystorageaccount\` in the same subscription.</span></span>

## <span data-ttu-id="82a8f-114">변수</span><span class="sxs-lookup"><span data-stu-id="82a8f-114">PARAMETERS</span></span>

### <span data-ttu-id="82a8f-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="82a8f-115">-EnableAdminUser</span></span>
<span data-ttu-id="82a8f-116">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-116">Enable admin user for the container registry.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a8f-117">-위치</span><span class="sxs-lookup"><span data-stu-id="82a8f-117">-Location</span></span>
<span data-ttu-id="82a8f-118">컨테이너 레지스트리 위치.</span><span class="sxs-lookup"><span data-stu-id="82a8f-118">Container Registry Location.</span></span>
<span data-ttu-id="82a8f-119">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="82a8f-120">-이름</span><span class="sxs-lookup"><span data-stu-id="82a8f-120">-Name</span></span>
<span data-ttu-id="82a8f-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-121">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistryName, RegistryName, ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a8f-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82a8f-122">-ResourceGroupName</span></span>
<span data-ttu-id="82a8f-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-123">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82a8f-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="82a8f-124">-Sku</span></span>
<span data-ttu-id="82a8f-125">컨테이너 레지스트리 SKU.</span><span class="sxs-lookup"><span data-stu-id="82a8f-125">Container Registry SKU.</span></span>
<span data-ttu-id="82a8f-126">허용 되는 값: Basic.</span><span class="sxs-lookup"><span data-stu-id="82a8f-126">Allowed values: Basic.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="82a8f-127">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="82a8f-127">-StorageAccountName</span></span>
<span data-ttu-id="82a8f-128">기존 저장소 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-128">The name of an existing storage account.</span></span>

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

### <span data-ttu-id="82a8f-129">태그</span><span class="sxs-lookup"><span data-stu-id="82a8f-129">-Tag</span></span>
<span data-ttu-id="82a8f-130">컨테이너 레지스트리 태그. 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-130">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="82a8f-131">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="82a8f-131">For example:</span></span>

<span data-ttu-id="82a8f-132">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="82a8f-132">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="82a8f-133">-확인</span><span class="sxs-lookup"><span data-stu-id="82a8f-133">-Confirm</span></span>
<span data-ttu-id="82a8f-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="82a8f-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="82a8f-135">-WhatIf</span></span>
<span data-ttu-id="82a8f-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="82a8f-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="82a8f-138">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a8f-138">-DefaultProfile</span></span>
<span data-ttu-id="82a8f-139">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="82a8f-139">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82a8f-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a8f-140">CommonParameters</span></span>
<span data-ttu-id="82a8f-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a8f-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="82a8f-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a8f-143">입력</span><span class="sxs-lookup"><span data-stu-id="82a8f-143">INPUTS</span></span>

### <span data-ttu-id="82a8f-144">않아야</span><span class="sxs-lookup"><span data-stu-id="82a8f-144">None</span></span>
<span data-ttu-id="82a8f-145">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="82a8f-145">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="82a8f-146">출력</span><span class="sxs-lookup"><span data-stu-id="82a8f-146">OUTPUTS</span></span>

### <span data-ttu-id="82a8f-147">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82a8f-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="82a8f-148">상속자</span><span class="sxs-lookup"><span data-stu-id="82a8f-148">NOTES</span></span>

## <span data-ttu-id="82a8f-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82a8f-149">RELATED LINKS</span></span>

[<span data-ttu-id="82a8f-150">Get-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82a8f-150">Get-AzureRmContainerRegistry</span></span>](Get-AzureRmContainerRegistry.md)

[<span data-ttu-id="82a8f-151">업데이트-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82a8f-151">Update-AzureRmContainerRegistry</span></span>](Update-AzureRmContainerRegistry.md)

[<span data-ttu-id="82a8f-152">제거-AzureRmContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="82a8f-152">Remove-AzureRmContainerRegistry</span></span>](Remove-AzureRmContainerRegistry.md)

