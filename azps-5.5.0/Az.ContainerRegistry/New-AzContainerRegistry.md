---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181457"
---
# <span data-ttu-id="5c2bb-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c2bb-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="5c2bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c2bb-102">SYNOPSIS</span></span>
<span data-ttu-id="5c2bb-103">컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-103">Creates a container registry.</span></span>

## <span data-ttu-id="5c2bb-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c2bb-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c2bb-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c2bb-105">DESCRIPTION</span></span>
<span data-ttu-id="5c2bb-106">New-AzContainerRegistry cmdlet은 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="5c2bb-107">예제</span><span class="sxs-lookup"><span data-stu-id="5c2bb-107">EXAMPLES</span></span>

### <span data-ttu-id="5c2bb-108">예제 1: 새 저장소 계정으로 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="5c2bb-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5c2bb-109">이 명령은 리소스 그룹 \` MyResourceGroup에 새 저장소 계정으로 컨테이너 레지스트리를 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="5c2bb-110">예제 2: 관리 사용자가 사용하도록 설정된 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="5c2bb-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="5c2bb-111">이 명령은 관리자 사용자가 사용하도록 설정된 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="5c2bb-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c2bb-112">PARAMETERS</span></span>

### <span data-ttu-id="5c2bb-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c2bb-113">-DefaultProfile</span></span>
<span data-ttu-id="5c2bb-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5c2bb-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5c2bb-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="5c2bb-115">-EnableAdminUser</span></span>
<span data-ttu-id="5c2bb-116">컨테이너 레지스트리에 대한 관리자 사용자를 사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-116">Enable admin user for the container registry.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: EnableAdmin

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2bb-117">-Location</span><span class="sxs-lookup"><span data-stu-id="5c2bb-117">-Location</span></span>
<span data-ttu-id="5c2bb-118">Container Registry 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-118">Container Registry Location.</span></span>
<span data-ttu-id="5c2bb-119">기본적으로 리소스 그룹의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="5c2bb-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5c2bb-120">-Name</span></span>
<span data-ttu-id="5c2bb-121">Container Registry 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="5c2bb-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c2bb-122">-ResourceGroupName</span></span>
<span data-ttu-id="5c2bb-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="5c2bb-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="5c2bb-124">-Sku</span></span>
<span data-ttu-id="5c2bb-125">Container Registry SKU입니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-125">Container Registry SKU.</span></span>
<span data-ttu-id="5c2bb-126">허용되는 값: Basic.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-126">Allowed values: Basic.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ContainerRegistrySku, RegistrySku
Accepted values: Basic, Premium, Standard

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5c2bb-127">-Tag</span><span class="sxs-lookup"><span data-stu-id="5c2bb-127">-Tag</span></span>
<span data-ttu-id="5c2bb-128">Container Registry Tags.Key-value 쌍(해시 테이블 형식).</span><span class="sxs-lookup"><span data-stu-id="5c2bb-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="5c2bb-129">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="5c2bb-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="5c2bb-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c2bb-130">-Confirm</span></span>
<span data-ttu-id="5c2bb-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c2bb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c2bb-132">-WhatIf</span></span>
<span data-ttu-id="5c2bb-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c2bb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c2bb-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c2bb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c2bb-135">CommonParameters</span></span>
<span data-ttu-id="5c2bb-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c2bb-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c2bb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c2bb-138">입력</span><span class="sxs-lookup"><span data-stu-id="5c2bb-138">INPUTS</span></span>

### <span data-ttu-id="5c2bb-139">System.String</span><span class="sxs-lookup"><span data-stu-id="5c2bb-139">System.String</span></span>

## <span data-ttu-id="5c2bb-140">출력</span><span class="sxs-lookup"><span data-stu-id="5c2bb-140">OUTPUTS</span></span>

### <span data-ttu-id="5c2bb-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c2bb-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="5c2bb-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c2bb-142">NOTES</span></span>

## <span data-ttu-id="5c2bb-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c2bb-143">RELATED LINKS</span></span>

[<span data-ttu-id="5c2bb-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c2bb-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="5c2bb-145">Update-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c2bb-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="5c2bb-146">Remove-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="5c2bb-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

