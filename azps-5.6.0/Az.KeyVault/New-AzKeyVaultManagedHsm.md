---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultManagedHsm.md
ms.openlocfilehash: 72804d546869f2d003813c8e69c067ad23966fa9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001307"
---
# <span data-ttu-id="3d8ed-101">New-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3d8ed-101">New-AzKeyVaultManagedHsm</span></span>

## <span data-ttu-id="3d8ed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3d8ed-102">SYNOPSIS</span></span>
<span data-ttu-id="3d8ed-103">관리되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-103">Creates a managed HSM.</span></span>

## <span data-ttu-id="3d8ed-104">구문</span><span class="sxs-lookup"><span data-stu-id="3d8ed-104">SYNTAX</span></span>

```
New-AzKeyVaultManagedHsm [-Name] <String> [-ResourceGroupName] <String> [-Location] <String>
 [-Administrator] <String[]> [-Sku <String>] [-Tag <Hashtable>] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3d8ed-105">설명</span><span class="sxs-lookup"><span data-stu-id="3d8ed-105">DESCRIPTION</span></span>
<span data-ttu-id="3d8ed-106">**New-AzKeyVaultManagedHsm** cmdlet은 지정된 리소스 그룹에 관리되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-106">The **New-AzKeyVaultManagedHsm** cmdlet creates a managed HSM in the specified resource group.</span></span> <span data-ttu-id="3d8ed-107">관리되는 HSM에서 키를 추가, 제거 또는 나열하려면 사용자에게 관리자에 사용자 ID를 추가하여 권한을 부여해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-107">To add, remove, or list keys in the managed HSM, user should grant permissions by adding user ID to Administrator.</span></span>

## <span data-ttu-id="3d8ed-108">예제</span><span class="sxs-lookup"><span data-stu-id="3d8ed-108">EXAMPLES</span></span>

### <span data-ttu-id="3d8ed-109">예제 1: StandardB1 관리 HSM 만들기</span><span class="sxs-lookup"><span data-stu-id="3d8ed-109">Example 1: Create a StandardB1 managed HSM</span></span>
```powershell
PS C:\> New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx"

Name  Resource Group Name Location    SKU
----  ------------------- --------    ---
myhsm myrg1               eastus2euap StandardB1
```

<span data-ttu-id="3d8ed-110">이 명령은 eastus2euap 위치에 myhsm이라는 관리되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-110">This command creates a managed HSM named myhsm in the location eastus2euap.</span></span> <span data-ttu-id="3d8ed-111">명령은 myrg1이라는 리소스 그룹에 관리되는 HSM을 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-111">The command adds the managed HSM to the resource group named myrg1.</span></span> <span data-ttu-id="3d8ed-112">명령은 *SKU* 매개 변수에 대한 값을 지정하지 않습니다. 관리되는 Standard_B1 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-112">Because the command does not specify a value for the *SKU* parameter, it creates a Standard_B1 managed HSM.</span></span>

### <span data-ttu-id="3d8ed-113">예제 2: CustomB32 관리형 HSM 만들기</span><span class="sxs-lookup"><span data-stu-id="3d8ed-113">Example 2: Create a CustomB32 managed HSM</span></span>
```powershell
PS C:\>New-AzKeyVaultManagedHsm -Name 'myhsm' -ResourceGroupName 'myrg1' -Location 'eastus2euap' -Administrator "xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx" -Sku 'CustomB32'
Name  Resource Group Name Location    SKU

----  ------------------- --------    ---
myhsm myrg1               eastus2euap CustomB32
```

                      

<span data-ttu-id="3d8ed-114">이 명령은 이전 예제와 마찬가지로 관리되는 HSM을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-114">This command creates a managed HSM, just like the previous example.</span></span> <span data-ttu-id="3d8ed-115">그러나 *SKU* 매개 변수에 대한 CustomB32 값을 지정하여 CustomB32 관리되는 HSM을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-115">However, it specifies a value of CustomB32 for the *SKU* parameter to create a CustomB32 managed HSM.</span></span>

## <span data-ttu-id="3d8ed-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3d8ed-116">PARAMETERS</span></span>

### <span data-ttu-id="3d8ed-117">-Administrator</span><span class="sxs-lookup"><span data-stu-id="3d8ed-117">-Administrator</span></span>
<span data-ttu-id="3d8ed-118">이 관리되는 HSM 풀에 대한 초기 관리자 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-118">Initial administrator object id for this managed HSM pool.</span></span>

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

### <span data-ttu-id="3d8ed-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3d8ed-119">-AsJob</span></span>
<span data-ttu-id="3d8ed-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3d8ed-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3d8ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3d8ed-121">-DefaultProfile</span></span>
<span data-ttu-id="3d8ed-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3d8ed-123">-Location</span><span class="sxs-lookup"><span data-stu-id="3d8ed-123">-Location</span></span>
<span data-ttu-id="3d8ed-124">키 자격 증명 모음을 만들 Azure 지역을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-124">Specifies the Azure region in which to create the key vault.</span></span>
<span data-ttu-id="3d8ed-125">ProviderNamespace Get-AzResourceProvider 명령을 사용하여 선택을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-125">Use the command Get-AzResourceProvider with the ProviderNamespace parameter to see your choices.</span></span>

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

### <span data-ttu-id="3d8ed-126">-Name</span><span class="sxs-lookup"><span data-stu-id="3d8ed-126">-Name</span></span>
<span data-ttu-id="3d8ed-127">만들 관리되는 HSM의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-127">Specifies a name of the managed HSM to create.</span></span>
<span data-ttu-id="3d8ed-128">이름은 문자, 숫자 또는 하이픈의 조합일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-128">The name can be any combination of letters, digits, or hyphens.</span></span>
<span data-ttu-id="3d8ed-129">이름은 문자 또는 숫자로 시작하고 끝내야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-129">The name must start and end with a letter or digit.</span></span>
<span data-ttu-id="3d8ed-130">이름은 보편적으로 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-130">The name must be universally unique.</span></span>

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

### <span data-ttu-id="3d8ed-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3d8ed-131">-ResourceGroupName</span></span>
<span data-ttu-id="3d8ed-132">키 자격 증명 모음을 만들 기존 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-132">Specifies the name of an existing resource group in which to create the key vault.</span></span>

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

### <span data-ttu-id="3d8ed-133">-Sku</span><span class="sxs-lookup"><span data-stu-id="3d8ed-133">-Sku</span></span>
<span data-ttu-id="3d8ed-134">관리되는 HSM 인스턴스의 SKU를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-134">Specifies the SKU of the managed HSM instance.</span></span>

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

### <span data-ttu-id="3d8ed-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="3d8ed-135">-Tag</span></span>
<span data-ttu-id="3d8ed-136">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-136">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="3d8ed-137">-확인</span><span class="sxs-lookup"><span data-stu-id="3d8ed-137">-Confirm</span></span>
<span data-ttu-id="3d8ed-138">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3d8ed-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3d8ed-139">-WhatIf</span></span>
<span data-ttu-id="3d8ed-140">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3d8ed-141">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3d8ed-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3d8ed-142">CommonParameters</span></span>
<span data-ttu-id="3d8ed-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3d8ed-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3d8ed-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3d8ed-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3d8ed-145">입력</span><span class="sxs-lookup"><span data-stu-id="3d8ed-145">INPUTS</span></span>

### <span data-ttu-id="3d8ed-146">System.String</span><span class="sxs-lookup"><span data-stu-id="3d8ed-146">System.String</span></span>

### <span data-ttu-id="3d8ed-147">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3d8ed-147">System.String[]</span></span>

### <span data-ttu-id="3d8ed-148">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3d8ed-148">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3d8ed-149">출력</span><span class="sxs-lookup"><span data-stu-id="3d8ed-149">OUTPUTS</span></span>

### <span data-ttu-id="3d8ed-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3d8ed-150">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="3d8ed-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3d8ed-151">NOTES</span></span>

## <span data-ttu-id="3d8ed-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3d8ed-152">RELATED LINKS</span></span>

[<span data-ttu-id="3d8ed-153">Get-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3d8ed-153">Get-AzKeyVaultManagedHsm</span></span>](./Get-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="3d8ed-154">Remove-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3d8ed-154">Remove-AzKeyVaultManagedHsm</span></span>](./Remove-AzKeyVaultManagedHsm.md)

[<span data-ttu-id="3d8ed-155">Update-AzKeyVaultManagedHsm</span><span class="sxs-lookup"><span data-stu-id="3d8ed-155">Update-AzKeyVaultManagedHsm</span></span>](./Update-AzKeyVaultManagedHsm.md)