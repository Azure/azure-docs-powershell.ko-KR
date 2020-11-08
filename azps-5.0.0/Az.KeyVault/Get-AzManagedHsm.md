---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsm.md
ms.openlocfilehash: 7a67d6aa0b891c78d644ec7d5f3923a354c3cef1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217727"
---
# <span data-ttu-id="19335-101">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="19335-101">Get-AzManagedHsm</span></span>

## <span data-ttu-id="19335-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19335-102">SYNOPSIS</span></span>
<span data-ttu-id="19335-103">관리 되는 Hsm을 받으세요.</span><span class="sxs-lookup"><span data-stu-id="19335-103">Get managed HSMs.</span></span>

## <span data-ttu-id="19335-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19335-104">SYNTAX</span></span>

```
Get-AzManagedHsm [[-Name] <String>] [[-ResourceGroupName] <String>] [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="19335-105">설명은</span><span class="sxs-lookup"><span data-stu-id="19335-105">DESCRIPTION</span></span>
<span data-ttu-id="19335-106">**AzManagedHsm** cmdlet은 구독에서 관리 되는 hsm에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19335-106">The **Get-AzManagedHsm** cmdlet gets information about the managed HSMs in a subscription.</span></span> <span data-ttu-id="19335-107">구독에서 관리 되는 모든 Hsm 인스턴스를 보거나 리소스 그룹 또는 특정 관리 되는 HSM을 기준으로 결과를 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="19335-107">You can view all managed HSMs instances in a subscription, or filter your results by a resource group or a particular managed HSM.</span></span>
<span data-ttu-id="19335-108">관리 되는 단일 HSM을 가져올 때이 cmdlet에 리소스 그룹을 지정 하는 것은 선택 사항 이지만 더 나은 성능을 위해서는이 작업을 수행 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="19335-108">Note that although specifying the resource group is optional for this cmdlet when you get a single managed HSM, you should do so for better performance.</span></span>

## <span data-ttu-id="19335-109">예제의</span><span class="sxs-lookup"><span data-stu-id="19335-109">EXAMPLES</span></span>

### <span data-ttu-id="19335-110">예제 1: 현재 구독에서 관리 되는 모든 Hsm 가져오기</span><span class="sxs-lookup"><span data-stu-id="19335-110">Example 1: Get all managed HSMs in your current subscription</span></span>
```powershell
PS C:\> Get-AzManagedHsm

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="19335-111">이 명령은 현재 구독에서 관리 되는 모든 Hsm을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19335-111">This command gets all managed HSMs in your current subscription.</span></span>

### <span data-ttu-id="19335-112">예제 2: 관리 되는 특정 HSM 가져오기</span><span class="sxs-lookup"><span data-stu-id="19335-112">Example 2: Get a specific managed HSM</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="19335-113">이 명령은 현재 구독에서 myhsm 이라는 관리 되는 HSM을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19335-113">This command gets the managed HSM named myhsm in your current subscription.</span></span>

### <span data-ttu-id="19335-114">예제 3: 리소스 그룹에 관리 되는 Hsm 가져오기</span><span class="sxs-lookup"><span data-stu-id="19335-114">Example 3: Get managed HSMs in a resource group</span></span>
```powershell
PS C:\> Get-AzManagedHsm -ResourceGroupName 'myrg1'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="19335-115">이 명령은 myrg1 이라는 리소스 그룹에 있는 모든 관리 되는 Hsm을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19335-115">This command gets all managed HSMs in the resource group named myrg1.</span></span>

### <span data-ttu-id="19335-116">예제 4: 필터링을 사용 하 여 관리 되는 Hsm 가져오기</span><span class="sxs-lookup"><span data-stu-id="19335-116">Example 4: Get managed HSMs using filtering</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name 'myhsm*'

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="19335-117">이 명령은 "myhsm"으로 시작 하는 구독의 관리 되는 모든 Hsm을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="19335-117">This command gets all managed HSMs in the subscription that start with "myhsm".</span></span>

## <span data-ttu-id="19335-118">변수</span><span class="sxs-lookup"><span data-stu-id="19335-118">PARAMETERS</span></span>

### <span data-ttu-id="19335-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19335-119">-DefaultProfile</span></span>
<span data-ttu-id="19335-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19335-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="19335-121">-이름</span><span class="sxs-lookup"><span data-stu-id="19335-121">-Name</span></span>
<span data-ttu-id="19335-122">HSM 이름.</span><span class="sxs-lookup"><span data-stu-id="19335-122">HSM name.</span></span> <span data-ttu-id="19335-123">Cmdlet은 이름 및 현재 선택 된 환경에 따라 HSM의 FQDN을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="19335-123">Cmdlet constructs the FQDN of a HSM based on the name and currently selected environment.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19335-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19335-124">-ResourceGroupName</span></span>
<span data-ttu-id="19335-125">쿼리 되는 관리 되는 HSM과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19335-125">Specifies the name of the resource group associated with the managed HSM being queried.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="19335-126">태그</span><span class="sxs-lookup"><span data-stu-id="19335-126">-Tag</span></span>
<span data-ttu-id="19335-127">관리 되는 Hsm 목록을 필터링 하는 지정 된 태그의 키 및 선택적 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="19335-127">Specifies the key and optional value of the specified tag to filter the list of managed HSMs by.</span></span>

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

### <span data-ttu-id="19335-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19335-128">CommonParameters</span></span>
<span data-ttu-id="19335-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19335-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19335-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="19335-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19335-131">입력</span><span class="sxs-lookup"><span data-stu-id="19335-131">INPUTS</span></span>

### <span data-ttu-id="19335-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19335-132">System.String</span></span>

### <span data-ttu-id="19335-133">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="19335-133">System.Collections.Hashtable</span></span>

## <span data-ttu-id="19335-134">출력</span><span class="sxs-lookup"><span data-stu-id="19335-134">OUTPUTS</span></span>

### <span data-ttu-id="19335-135">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="19335-135">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="19335-136">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="19335-136">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

## <span data-ttu-id="19335-137">상속자</span><span class="sxs-lookup"><span data-stu-id="19335-137">NOTES</span></span>

## <span data-ttu-id="19335-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19335-138">RELATED LINKS</span></span>

[<span data-ttu-id="19335-139">새로운 AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="19335-139">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="19335-140">제거-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="19335-140">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="19335-141">업데이트-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="19335-141">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)