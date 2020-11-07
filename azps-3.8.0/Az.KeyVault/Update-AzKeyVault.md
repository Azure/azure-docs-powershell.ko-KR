---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 8932402fb9e4e6b27f284313bfddc764192c5e93
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878257"
---
# <span data-ttu-id="05c7b-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="05c7b-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="05c7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05c7b-102">SYNOPSIS</span></span>
<span data-ttu-id="05c7b-103">Azure 키 보관소의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="05c7b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05c7b-104">SYNTAX</span></span>

### <span data-ttu-id="05c7b-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="05c7b-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c7b-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c7b-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="05c7b-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="05c7b-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnableSoftDelete] [-EnablePurgeProtection]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05c7b-108">설명은</span><span class="sxs-lookup"><span data-stu-id="05c7b-108">DESCRIPTION</span></span>
<span data-ttu-id="05c7b-109">이 cmdlet은 Azure 키 자격 증명 모음의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-109">This cmdlet updates the state of an Azure key vault.</span></span>
<span data-ttu-id="05c7b-110">예를 들어, 소프트 삭제를 사용 하도록 설정 하면 일부 속성을 업데이트 하는 것은 취소할 수 없으며, 더 이상 비활성화 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-110">Please note updating some of the properties is an irreversible action, for example once soft delete has been enabled, it cannot be disabled anymore.</span></span>

## <span data-ttu-id="05c7b-111">예제의</span><span class="sxs-lookup"><span data-stu-id="05c7b-111">EXAMPLES</span></span>

### <span data-ttu-id="05c7b-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="05c7b-112">Example 1</span></span>
```powershell
PS C:\> Update-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName -EnableSoftDelete
```

<span data-ttu-id="05c7b-113">리소스 그룹에 명명 된 키 보관소에 대해 일시 삭제를 사용 하도록 설정 `$keyVaultName` `$resourceGroupName` 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-113">Enables soft delete on the key vault named `$keyVaultName` in resource group `$resourceGroupName`.</span></span>

### <span data-ttu-id="05c7b-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="05c7b-114">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="05c7b-115">파이핑 구문을 사용한 지우기 보호를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-115">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="05c7b-116">변수</span><span class="sxs-lookup"><span data-stu-id="05c7b-116">PARAMETERS</span></span>

### <span data-ttu-id="05c7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05c7b-117">-DefaultProfile</span></span>
<span data-ttu-id="05c7b-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-119">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="05c7b-119">-EnablePurgeProtection</span></span>
<span data-ttu-id="05c7b-120">이 키 자격 증명 모음에 대 한 보호 제거 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-120">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="05c7b-121">활성화 한 후에는 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-121">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="05c7b-122">이 기능을 사용 하려면 소프트 삭제가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-122">It requires soft-delete to be turned on.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-123">-EnableSoftDelete</span><span class="sxs-lookup"><span data-stu-id="05c7b-123">-EnableSoftDelete</span></span>
<span data-ttu-id="05c7b-124">이 키 자격 증명 모음에 대 한 소프트 삭제 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-124">Enable the soft-delete functionality for this key vault.</span></span>
<span data-ttu-id="05c7b-125">활성화 한 후에는 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-125">Once enabled it cannot be disabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05c7b-126">-InputObject</span></span>
<span data-ttu-id="05c7b-127">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="05c7b-127">Key vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05c7b-128">-ResourceGroupName</span></span>
<span data-ttu-id="05c7b-129">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-129">Name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-130">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="05c7b-130">-ResourceId</span></span>
<span data-ttu-id="05c7b-131">키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-131">Resource ID of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-132">-VaultName</span><span class="sxs-lookup"><span data-stu-id="05c7b-132">-VaultName</span></span>
<span data-ttu-id="05c7b-133">키 보관소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-133">Name of the key vault.</span></span>

```yaml
Type: String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-134">-확인</span><span class="sxs-lookup"><span data-stu-id="05c7b-134">-Confirm</span></span>
<span data-ttu-id="05c7b-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05c7b-136">-WhatIf</span></span>
<span data-ttu-id="05c7b-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05c7b-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05c7b-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05c7b-139">CommonParameters</span></span>
<span data-ttu-id="05c7b-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05c7b-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05c7b-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05c7b-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05c7b-142">입력</span><span class="sxs-lookup"><span data-stu-id="05c7b-142">INPUTS</span></span>

### <span data-ttu-id="05c7b-143">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="05c7b-143">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="05c7b-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="05c7b-144">System.String</span></span>

## <span data-ttu-id="05c7b-145">출력</span><span class="sxs-lookup"><span data-stu-id="05c7b-145">OUTPUTS</span></span>

### <span data-ttu-id="05c7b-146">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="05c7b-146">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="05c7b-147">상속자</span><span class="sxs-lookup"><span data-stu-id="05c7b-147">NOTES</span></span>

## <span data-ttu-id="05c7b-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05c7b-148">RELATED LINKS</span></span>
