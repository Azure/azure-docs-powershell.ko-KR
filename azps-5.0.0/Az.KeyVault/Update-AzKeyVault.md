---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/update-azkeyvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Update-AzKeyVault.md
ms.openlocfilehash: 10a441cd1354b75a13b429c4375e7bc3fba72244
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215276"
---
# <span data-ttu-id="8f5eb-101">Update-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="8f5eb-101">Update-AzKeyVault</span></span>

## <span data-ttu-id="8f5eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8f5eb-102">SYNOPSIS</span></span>
<span data-ttu-id="8f5eb-103">Azure 키 보관소의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-103">Update the state of an Azure key vault.</span></span>

## <span data-ttu-id="8f5eb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8f5eb-104">SYNTAX</span></span>

### <span data-ttu-id="8f5eb-105">UpdateByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="8f5eb-105">UpdateByNameParameterSet (Default)</span></span>
```
Update-AzKeyVault -ResourceGroupName <String> -VaultName <String> [-EnablePurgeProtection]
 [-EnableRbacAuthorization <Boolean>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8f5eb-106">UpdateByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f5eb-106">UpdateByInputObjectParameterSet</span></span>
```
Update-AzKeyVault -InputObject <PSKeyVault> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8f5eb-107">UpdateByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="8f5eb-107">UpdateByResourceIdParameterSet</span></span>
```
Update-AzKeyVault -ResourceId <String> [-EnablePurgeProtection] [-EnableRbacAuthorization <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8f5eb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8f5eb-108">DESCRIPTION</span></span>
<span data-ttu-id="8f5eb-109">이 cmdlet은 Azure 키 자격 증명 모음의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-109">This cmdlet updates the state of an Azure key vault.</span></span>

## <span data-ttu-id="8f5eb-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8f5eb-110">EXAMPLES</span></span>

### <span data-ttu-id="8f5eb-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="8f5eb-111">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVault -VaultName $keyVaultName -ResourceGroupName $resourceGroupName | Update-AzKeyVault -EnablePurgeProtection
```

<span data-ttu-id="8f5eb-112">파이핑 구문을 사용한 지우기 보호를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-112">Enables purge protection using piping syntax.</span></span>

## <span data-ttu-id="8f5eb-113">변수</span><span class="sxs-lookup"><span data-stu-id="8f5eb-113">PARAMETERS</span></span>

### <span data-ttu-id="8f5eb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8f5eb-114">-DefaultProfile</span></span>
<span data-ttu-id="8f5eb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8f5eb-116">-EnablePurgeProtection</span><span class="sxs-lookup"><span data-stu-id="8f5eb-116">-EnablePurgeProtection</span></span>
<span data-ttu-id="8f5eb-117">이 키 자격 증명 모음에 대 한 보호 제거 기능을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-117">Enable the purge protection functionality for this key vault.</span></span>
<span data-ttu-id="8f5eb-118">활성화 한 후에는 사용 하지 않도록 설정할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-118">Once enabled it cannot be disabled.</span></span>
<span data-ttu-id="8f5eb-119">이 기능을 사용 하려면 소프트 삭제가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-119">It requires soft-delete to be turned on.</span></span>

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

### <span data-ttu-id="8f5eb-120">-EnableRbacAuthorization</span><span class="sxs-lookup"><span data-stu-id="8f5eb-120">-EnableRbacAuthorization</span></span>
<span data-ttu-id="8f5eb-121">이 키 보관소를 사용 하거나 사용 하지 않도록 설정 하 여 역할별 (역할 기반 액세스 제어)로 데이터 작업을 승인 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-121">Enable or disable this key vault to authorize data actions by Role Based Access Control (RBAC).</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5eb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8f5eb-122">-InputObject</span></span>
<span data-ttu-id="8f5eb-123">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="8f5eb-123">Key vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: UpdateByInputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8f5eb-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8f5eb-124">-ResourceGroupName</span></span>
<span data-ttu-id="8f5eb-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-125">Name of the resource group.</span></span>

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

### <span data-ttu-id="8f5eb-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="8f5eb-126">-ResourceId</span></span>
<span data-ttu-id="8f5eb-127">키 자격 증명 모음의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-127">Resource ID of the key vault.</span></span>

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

### <span data-ttu-id="8f5eb-128">-VaultName</span><span class="sxs-lookup"><span data-stu-id="8f5eb-128">-VaultName</span></span>
<span data-ttu-id="8f5eb-129">키 보관소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-129">Name of the key vault.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8f5eb-130">-확인</span><span class="sxs-lookup"><span data-stu-id="8f5eb-130">-Confirm</span></span>
<span data-ttu-id="8f5eb-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8f5eb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8f5eb-132">-WhatIf</span></span>
<span data-ttu-id="8f5eb-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8f5eb-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8f5eb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8f5eb-135">CommonParameters</span></span>
<span data-ttu-id="8f5eb-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8f5eb-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8f5eb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8f5eb-138">입력</span><span class="sxs-lookup"><span data-stu-id="8f5eb-138">INPUTS</span></span>

### <span data-ttu-id="8f5eb-139">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8f5eb-139">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="8f5eb-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8f5eb-140">System.String</span></span>

## <span data-ttu-id="8f5eb-141">출력</span><span class="sxs-lookup"><span data-stu-id="8f5eb-141">OUTPUTS</span></span>

### <span data-ttu-id="8f5eb-142">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="8f5eb-142">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="8f5eb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="8f5eb-143">NOTES</span></span>

## <span data-ttu-id="8f5eb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8f5eb-144">RELATED LINKS</span></span>
