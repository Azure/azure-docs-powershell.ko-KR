---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistry.md
ms.openlocfilehash: 0f1e95c97076c13ed74c1ee708577a2429bcb979
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304139"
---
# <span data-ttu-id="7e3ea-101">New-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e3ea-101">New-AzContainerRegistry</span></span>

## <span data-ttu-id="7e3ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7e3ea-102">SYNOPSIS</span></span>
<span data-ttu-id="7e3ea-103">컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-103">Creates a container registry.</span></span>

## <span data-ttu-id="7e3ea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7e3ea-104">SYNTAX</span></span>

```
New-AzContainerRegistry [-ResourceGroupName] <String> [-Name] <String> [-Sku] <String> [-Location <String>]
 [-EnableAdminUser] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7e3ea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7e3ea-105">DESCRIPTION</span></span>
<span data-ttu-id="7e3ea-106">New-AzContainerRegistry cmdlet은 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-106">The New-AzContainerRegistry cmdlet creates a container registry.</span></span>

## <span data-ttu-id="7e3ea-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7e3ea-107">EXAMPLES</span></span>

### <span data-ttu-id="7e3ea-108">예제 1: 새 저장소 계정으로 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="7e3ea-108">Example 1: Create a container registry with a new storage account.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic"

   Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="7e3ea-109">이 명령은 리소스 그룹 myresourcegroup에 새 저장소 계정이 있는 컨테이너 레지스트리를 만듭니다 \` \` .</span><span class="sxs-lookup"><span data-stu-id="7e3ea-109">This command creates a container registry with a new storage account in the resource group \`MyResourceGroup\`.</span></span>

### <span data-ttu-id="7e3ea-110">예제 2: 관리자가 사용 하도록 설정 된 컨테이너 레지스트리 만들기</span><span class="sxs-lookup"><span data-stu-id="7e3ea-110">Example 2: Create a container registry with admin user enabled.</span></span>
```powershell
PS C:\>New-AzContainerRegistry -ResourceGroupName "MyResourceGroup" -Name "MyRegistry" -Sku "Basic" -EnableAdminUser

  Container registry location: eastus

Registry Name     Sku        LoginServer               CreationDate               Provisioni AdminUserE StorageAccountN
                                                                                  ngState    nabled     ame
-------------     ---        -----------               ------------               ---------- ---------- ---------------
myregistry        Premium    myregistry.azurecr.io     10/31/2017 6:49:31 PM      Succeeded  True
```

<span data-ttu-id="7e3ea-111">이 명령은 관리자 사용자가 설정 된 컨테이너 레지스트리를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-111">This command creates a container registry with admin user enabled.</span></span>

## <span data-ttu-id="7e3ea-112">변수</span><span class="sxs-lookup"><span data-stu-id="7e3ea-112">PARAMETERS</span></span>

### <span data-ttu-id="7e3ea-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7e3ea-113">-DefaultProfile</span></span>
<span data-ttu-id="7e3ea-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7e3ea-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7e3ea-115">-EnableAdminUser</span><span class="sxs-lookup"><span data-stu-id="7e3ea-115">-EnableAdminUser</span></span>
<span data-ttu-id="7e3ea-116">컨테이너 레지스트리에 관리자 사용자를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-116">Enable admin user for the container registry.</span></span>

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

### <span data-ttu-id="7e3ea-117">-위치</span><span class="sxs-lookup"><span data-stu-id="7e3ea-117">-Location</span></span>
<span data-ttu-id="7e3ea-118">컨테이너 레지스트리 위치.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-118">Container Registry Location.</span></span>
<span data-ttu-id="7e3ea-119">리소스 그룹의 위치를 기본값으로 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-119">Default to the location of the resource group.</span></span>

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

### <span data-ttu-id="7e3ea-120">-이름</span><span class="sxs-lookup"><span data-stu-id="7e3ea-120">-Name</span></span>
<span data-ttu-id="7e3ea-121">컨테이너 레지스트리 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-121">Container Registry Name.</span></span>

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

### <span data-ttu-id="7e3ea-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7e3ea-122">-ResourceGroupName</span></span>
<span data-ttu-id="7e3ea-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-123">Resource Group Name.</span></span>

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

### <span data-ttu-id="7e3ea-124">-Sku</span><span class="sxs-lookup"><span data-stu-id="7e3ea-124">-Sku</span></span>
<span data-ttu-id="7e3ea-125">컨테이너 레지스트리 SKU.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-125">Container Registry SKU.</span></span>
<span data-ttu-id="7e3ea-126">허용 되는 값: Basic.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-126">Allowed values: Basic.</span></span>

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

### <span data-ttu-id="7e3ea-127">태그</span><span class="sxs-lookup"><span data-stu-id="7e3ea-127">-Tag</span></span>
<span data-ttu-id="7e3ea-128">컨테이너 레지스트리 태그. 해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-128">Container Registry Tags.Key-value pairs in the form of a hash table.</span></span>
<span data-ttu-id="7e3ea-129">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="7e3ea-129">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="7e3ea-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7e3ea-130">-Confirm</span></span>
<span data-ttu-id="7e3ea-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7e3ea-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7e3ea-132">-WhatIf</span></span>
<span data-ttu-id="7e3ea-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7e3ea-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7e3ea-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7e3ea-135">CommonParameters</span></span>
<span data-ttu-id="7e3ea-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7e3ea-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7e3ea-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7e3ea-138">입력</span><span class="sxs-lookup"><span data-stu-id="7e3ea-138">INPUTS</span></span>

### <span data-ttu-id="7e3ea-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7e3ea-139">System.String</span></span>

## <span data-ttu-id="7e3ea-140">출력</span><span class="sxs-lookup"><span data-stu-id="7e3ea-140">OUTPUTS</span></span>

### <span data-ttu-id="7e3ea-141">ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e3ea-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

## <span data-ttu-id="7e3ea-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7e3ea-142">NOTES</span></span>

## <span data-ttu-id="7e3ea-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7e3ea-143">RELATED LINKS</span></span>

[<span data-ttu-id="7e3ea-144">Get-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e3ea-144">Get-AzContainerRegistry</span></span>](Get-AzContainerRegistry.md)

[<span data-ttu-id="7e3ea-145">업데이트-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e3ea-145">Update-AzContainerRegistry</span></span>](Update-AzContainerRegistry.md)

[<span data-ttu-id="7e3ea-146">제거-AzContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7e3ea-146">Remove-AzContainerRegistry</span></span>](Remove-AzContainerRegistry.md)

