---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azmanagedhsm
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzManagedHsm.md
ms.openlocfilehash: 49e8e5aeddba1b15c97155a200413ea774c8a7a5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226905"
---
# <span data-ttu-id="dad33-101">Update-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dad33-101">Update-AzManagedHsm</span></span>

## <span data-ttu-id="dad33-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dad33-102">SYNOPSIS</span></span>
<span data-ttu-id="dad33-103">Azure 관리 HSM의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-103">Update the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="dad33-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dad33-104">SYNTAX</span></span>

### <span data-ttu-id="dad33-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dad33-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzManagedHsm -Name <String> -ResourceGroupName <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad33-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dad33-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzManagedHsm -InputObject <PSManagedHsm> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dad33-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dad33-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzManagedHsm -ResourceId <String> [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dad33-108">설명은</span><span class="sxs-lookup"><span data-stu-id="dad33-108">DESCRIPTION</span></span>
<span data-ttu-id="dad33-109">이 cmdlet은 Azure 관리 HSM의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-109">This cmdlet updates the state of an Azure managed HSM.</span></span>

## <span data-ttu-id="dad33-110">예제의</span><span class="sxs-lookup"><span data-stu-id="dad33-110">EXAMPLES</span></span>

### <span data-ttu-id="dad33-111">예제 1: 관리 되는 Hsm을 직접 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-111">Example 1: Update a managed Hsm directly</span></span>
```powershell
PS C:\> Update-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName -Tag @{testKey="testValue"} | fl

Managed HSM Name                    : testmhsm
Resource Group Name                 : testmhsm
Location                            : eastus2euap
Resource ID                         : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/resourceGroups/testmhsm/provid
                                      ers/Microsoft.KeyVault/managedHSMs/testmhsm
HSM Pool URI                        :
Tenant ID                           : xxxxxx-xxxx-xxxx-xxxxxxxxxxxx
Initial Admin Object Ids            : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx
SKU                                 : StandardB1
Soft Delete Enabled?                : True
Enabled Purge Protection?           : False
Soft Delete Retention Period (days) : 90
Provisioning State                  : Provisioning
Status Message                      : Resource creation in progress. Starting service...
Tags                                :
                                      Name        Value
                                      ====        =====
                                      testKey     testValued
```

<span data-ttu-id="dad33-112">리소스 그룹에서 이름이 지정 된 관리 되는 Hsm에 대 한 태그를 업데이트 `$hsmName` `$resourceGroupName` 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-112">Updates tags for the managed Hsm named `$hsmName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="dad33-113">예제 2: 파이핑을 사용 하 여 관리 되는 Hsm 업데이트</span><span class="sxs-lookup"><span data-stu-id="dad33-113">Example 2: Update a managed Hsm using piping</span></span>
```powershell
PS C:\> Get-AzManagedHsm -Name $hsmName -ResourceGroupName $resourceGroupName | Update-AzManagedHsm -Tag @{testKey="testValue"}
```

<span data-ttu-id="dad33-114">파이핑 구문을 사용 하 여 관리 되는 Hsm의 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-114">Updates tags for the managed Hsm using piping syntax.</span></span>

## <span data-ttu-id="dad33-115">변수</span><span class="sxs-lookup"><span data-stu-id="dad33-115">PARAMETERS</span></span>

### <span data-ttu-id="dad33-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dad33-116">-DefaultProfile</span></span>
<span data-ttu-id="dad33-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dad33-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dad33-118">-InputObject</span></span>
<span data-ttu-id="dad33-119">관리 되는 HSM 개체.</span><span class="sxs-lookup"><span data-stu-id="dad33-119">Managed HSM object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dad33-120">-이름</span><span class="sxs-lookup"><span data-stu-id="dad33-120">-Name</span></span>
<span data-ttu-id="dad33-121">관리 되는 HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-121">Name of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: HsmName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad33-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dad33-122">-ResourceGroupName</span></span>
<span data-ttu-id="dad33-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-123">Name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dad33-124">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dad33-124">-ResourceId</span></span>
<span data-ttu-id="dad33-125">관리 되는 HSM의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-125">Resource ID of the managed HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dad33-126">태그</span><span class="sxs-lookup"><span data-stu-id="dad33-126">-Tag</span></span>
<span data-ttu-id="dad33-127">리소스 태그를 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-127">A hash table which represents resource tags.</span></span>

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

### <span data-ttu-id="dad33-128">-확인</span><span class="sxs-lookup"><span data-stu-id="dad33-128">-Confirm</span></span>
<span data-ttu-id="dad33-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dad33-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dad33-130">-WhatIf</span></span>
<span data-ttu-id="dad33-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dad33-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dad33-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dad33-133">CommonParameters</span></span>
<span data-ttu-id="dad33-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dad33-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dad33-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dad33-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dad33-136">입력</span><span class="sxs-lookup"><span data-stu-id="dad33-136">INPUTS</span></span>

### <span data-ttu-id="dad33-137">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dad33-137">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

### <span data-ttu-id="dad33-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dad33-138">System.String</span></span>

### <span data-ttu-id="dad33-139">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="dad33-139">System.Collections.Hashtable</span></span>

## <span data-ttu-id="dad33-140">출력</span><span class="sxs-lookup"><span data-stu-id="dad33-140">OUTPUTS</span></span>

### <span data-ttu-id="dad33-141">Microsoft. KeyVault. 모델. PSManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dad33-141">Microsoft.Azure.Commands.KeyVault.Models.PSManagedHsm</span></span>

## <span data-ttu-id="dad33-142">상속자</span><span class="sxs-lookup"><span data-stu-id="dad33-142">NOTES</span></span>

## <span data-ttu-id="dad33-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dad33-143">RELATED LINKS</span></span>

[<span data-ttu-id="dad33-144">새로운 AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dad33-144">New-AzManagedHsm</span></span>](./New-AzManagedHsm.md)

[<span data-ttu-id="dad33-145">제거-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dad33-145">Remove-AzManagedHsm</span></span>](./Remove-AzManagedHsm.md)

[<span data-ttu-id="dad33-146">Get-AzManagedHsm</span><span class="sxs-lookup"><span data-stu-id="dad33-146">Get-AzManagedHsm</span></span>](./Get-AzManagedHsm.md)