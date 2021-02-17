---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 8d602e5cbb3a24307ba77daf9a88a79a3c5bb705
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180444"
---
# <span data-ttu-id="4f5a4-101">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4f5a4-101">Get-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="4f5a4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f5a4-102">SYNOPSIS</span></span>
<span data-ttu-id="4f5a4-103">관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-103">Get managed HSMs.</span></span>

## <span data-ttu-id="4f5a4-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f5a4-104">SYNTAX</span></span>

```
Get-AzKeyVaultManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f5a4-105">설명</span><span class="sxs-lookup"><span data-stu-id="4f5a4-105">DESCRIPTION</span></span>
<span data-ttu-id="4f5a4-106">**Get-AzKeyVaultManagedHsm** cmdlet은 구독에서 관리되는 HSM에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-106">The **Get-AzKeyVaultManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="4f5a4-107">구독에서 모든 관리되는 HSM 인스턴스를 보거나 리소스 그룹 또는 특정 관리되는 HSM을 통해 결과를 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="4f5a4-108">단일 관리되는 HSM을 얻을 때 이 cmdlet에 대해 리소스 그룹을 지정하는 것은 선택 사항이지만 성능을 향상하기 위해 이 작업을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="4f5a4-109">예제</span><span class="sxs-lookup"><span data-stu-id="4f5a4-109">EXAMPLES</span></span>

### <span data-ttu-id="4f5a4-110">예제 1: 현재 구독에서 관리되는 모든 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4f5a4-111">이 명령은 현재 구독의 모든 관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="4f5a4-112">예제 2: 특정 관리형 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4f5a4-113">이 명령은 현재 구독에서 myhsm이라는 관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="4f5a4-114">예제 3: 리소스 그룹에서 관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4f5a4-115">이 명령은 myrg1이라는 리소스 그룹의 모든 관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="4f5a4-116">예제 4: 필터링을 사용하여 관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzKeyVaultManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="4f5a4-117">이 명령은 "myhsm"으로 시작하는 구독의 모든 관리되는 HSM을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="4f5a4-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f5a4-118">PARAMETERS</span></span>

### <span data-ttu-id="4f5a4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f5a4-119">-DefaultProfile</span></span>
<span data-ttu-id="4f5a4-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f5a4-121">-Name</span><span class="sxs-lookup"><span data-stu-id="4f5a4-121">-Name</span></span>
<span data-ttu-id="4f5a4-122">HSM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-122">HSM name.</span></span> <span data-ttu-id="4f5a4-123">Cmdlet은 이름 및 현재 선택한 환경에 따라 HSM의 FQDN을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4f5a4-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f5a4-124">-ResourceGroupName</span></span>
<span data-ttu-id="4f5a4-125">관리되는 HSM과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4f5a4-126">-Tag</span><span class="sxs-lookup"><span data-stu-id="4f5a4-126">-Tag</span></span>
<span data-ttu-id="4f5a4-127">관리되는 HSM 목록을 필터링하기 위해 지정된 태그의 키 및 선택적 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4f5a4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f5a4-128">CommonParameters</span></span>
<span data-ttu-id="4f5a4-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f5a4-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4f5a4-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f5a4-131">입력</span><span class="sxs-lookup"><span data-stu-id="4f5a4-131">INPUTS</span></span>

### <span data-ttu-id="4f5a4-132">System.String</span><span class="sxs-lookup"><span data-stu-id="4f5a4-132">System.String</span></span>

### <span data-ttu-id="4f5a4-133">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="4f5a4-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="4f5a4-134">출력</span><span class="sxs-lookup"><span data-stu-id="4f5a4-134">OUTPUTS</span></span>

### <span data-ttu-id="4f5a4-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4f5a4-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="4f5a4-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="4f5a4-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="4f5a4-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f5a4-137">NOTES</span></span>

## <span data-ttu-id="4f5a4-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f5a4-138">RELATED LINKS</span></span>

[<span data-ttu-id="4f5a4-139">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4f5a4-139">New-AzKeyVaultManagedHsm</span></span>](./New-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4f5a4-140">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4f5a4-140">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="4f5a4-141">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="4f5a4-141">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)