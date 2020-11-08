---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsm.md
ms.openlocfilehash: 2cab0fedd31f482b2e826a02f686ec8bf651c1bb
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226928"
---
# <span data-ttu-id="e8be6-101">New-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e8be6-101">New-AzManagedHsm</span></span>

## <span data-ttu-id="e8be6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8be6-102">SYNOPSIS</span></span>
<span data-ttu-id="e8be6-103">관리 되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="e8be6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e8be6-104">SYNTAX</span></span>

```
New-AzManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8be6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e8be6-105">DESCRIPTION</span></span>
<span data-ttu-id="e8be6-106">**AzManagedHsm** cmdlet은 지정 된 리소스 그룹에 관리 되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-106">The **New-AzManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="e8be6-107">관리 되는 HSM에서 키를 추가, 제거 또는 나열 하려면 사용자 ID를 관리자에 추가 하 여 권한을 부여 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="e8be6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="e8be6-108">EXAMPLES</span></span>

### <span data-ttu-id="e8be6-109">예제 1: StandardB1 관리 되는 HSM 만들기</span><span class="sxs-lookup"><span data-stu-id="e8be6-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="e8be6-110">이 명령은 위치 eastus2euap에 myhsm 이라는 관리 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="e8be6-111">명령이 myrg1 이라는 리소스 그룹에 관리 되는 HSM을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="e8be6-112">명령이 *SKU* 매개 변수에 대 한 값을 지정 하지 않기 때문에 Standard_B1 관리 되는 HSM이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="e8be6-113">예제 2: CustomB32 관리 HSM 만들기</span><span class="sxs-lookup"><span data-stu-id="e8be6-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="e8be6-114">이 명령은 이전 예제와 마찬가지로 관리 되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="e8be6-115">그러나 *SKU* 매개 변수에 대 한 CustomB32 값을 지정 하 여 CustomB32 관리 되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="e8be6-116">변수</span><span class="sxs-lookup"><span data-stu-id="e8be6-116">PARAMETERS</span></span>

### <span data-ttu-id="e8be6-117">-관리자</span><span class="sxs-lookup"><span data-stu-id="e8be6-117">-Administrator</span></span>
<span data-ttu-id="e8be6-118">이 관리 되는 HSM 풀의 초기 관리자 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-118">Initial administrator object id for this managed HSM pool.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="e8be6-119">-AsJob</span></span>
<span data-ttu-id="e8be6-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="e8be6-120">Run cmdlet in the background</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8be6-121">-DefaultProfile</span></span>
<span data-ttu-id="e8be6-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e8be6-123">-위치</span><span class="sxs-lookup"><span data-stu-id="e8be6-123">-Location</span></span>
<span data-ttu-id="e8be6-124">키 자격 증명 모음을 만들 Azure 지역을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="e8be6-125">명령 Get-AzResourceProvider를 ProviderNamespace 매개 변수와 함께 사용 하 여 선택 항목을 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-126">-이름</span><span class="sxs-lookup"><span data-stu-id="e8be6-126">-Name</span></span>
<span data-ttu-id="e8be6-127">만들려는 관리 되는 HSM의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="e8be6-128">이름은 문자, 숫자 또는 하이픈을 임의로 조합 하 여 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="e8be6-129">이름은 문자 또는 숫자로 시작 하 고 끝나야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="e8be6-130">이름은 범용으로 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-130">The name must be universally unique.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HsmName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8be6-131">-ResourceGroupName</span></span>
<span data-ttu-id="e8be6-132">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="e8be6-133">-Sku</span></span>
<span data-ttu-id="e8be6-134">관리 되는 HSM 인스턴스의 SKU를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-134">Specifies the SKU of the managed HSM instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-135">태그</span><span class="sxs-lookup"><span data-stu-id="e8be6-135">-Tag</span></span>
<span data-ttu-id="e8be6-136">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-136">A hash table which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8be6-137">-확인</span><span class="sxs-lookup"><span data-stu-id="e8be6-137">-Confirm</span></span>
<span data-ttu-id="e8be6-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8be6-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8be6-139">-WhatIf</span></span>
<span data-ttu-id="e8be6-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8be6-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8be6-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8be6-142">CommonParameters</span></span>
<span data-ttu-id="e8be6-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e8be6-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8be6-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="e8be6-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8be6-145">입력</span><span class="sxs-lookup"><span data-stu-id="e8be6-145">INPUTS</span></span>

### <span data-ttu-id="e8be6-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e8be6-146">System.String</span></span>

### <span data-ttu-id="e8be6-147">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e8be6-147">System.String[]</span></span>

### <span data-ttu-id="e8be6-148">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e8be6-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e8be6-149">출력</span><span class="sxs-lookup"><span data-stu-id="e8be6-149">OUTPUTS</span></span>

### <span data-ttu-id="e8be6-150">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e8be6-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="e8be6-151">상속자</span><span class="sxs-lookup"><span data-stu-id="e8be6-151">NOTES</span></span>

## <span data-ttu-id="e8be6-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e8be6-152">RELATED LINKS</span></span>

[<span data-ttu-id="e8be6-153">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e8be6-153">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)

[<span data-ttu-id="e8be6-154">제거-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e8be6-154">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="e8be6-155">업데이트-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="e8be6-155">Update-AzManagedHsm</span></span>](./Update-AzManagedHsm.md)