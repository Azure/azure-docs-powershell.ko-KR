---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 564c3d9a67e3a006a7ce7871419e236a71838a42
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101965216"
---
# <span data-ttu-id="80ba8-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="80ba8-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="80ba8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="80ba8-102">SYNOPSIS</span></span>
<span data-ttu-id="80ba8-103">토의를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-103">Deletes an attestation.</span></span>

## <span data-ttu-id="80ba8-104">구문</span><span class="sxs-lookup"><span data-stu-id="80ba8-104">SYNTAX</span></span>

### <span data-ttu-id="80ba8-105">ByAvailableAttestation(기본값)</span><span class="sxs-lookup"><span data-stu-id="80ba8-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80ba8-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="80ba8-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="80ba8-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="80ba8-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="80ba8-108">설명</span><span class="sxs-lookup"><span data-stu-id="80ba8-108">DESCRIPTION</span></span>
<span data-ttu-id="80ba8-109">Remove-AzAttestation cmdlet은 지정된 데이터 를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="80ba8-110">예제</span><span class="sxs-lookup"><span data-stu-id="80ba8-110">EXAMPLES</span></span>

### <span data-ttu-id="80ba8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="80ba8-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="80ba8-112">현재 구독에서 *psh-test-rg라는 리소스* 그룹에서 *pshtest3이라는* 테스트 공급자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="80ba8-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="80ba8-113">PARAMETERS</span></span>

### <span data-ttu-id="80ba8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="80ba8-114">-DefaultProfile</span></span>
<span data-ttu-id="80ba8-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="80ba8-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="80ba8-116">-InputObject</span></span>
<span data-ttu-id="80ba8-117">삭제할 수 있는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-117">Attestation object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Attestation.Models.PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="80ba8-118">-Name</span><span class="sxs-lookup"><span data-stu-id="80ba8-118">-Name</span></span>
<span data-ttu-id="80ba8-119">제거할 명단의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-119">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ba8-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="80ba8-120">-PassThru</span></span>
<span data-ttu-id="80ba8-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="80ba8-122">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="80ba8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="80ba8-123">-ResourceGroupName</span></span>
<span data-ttu-id="80ba8-124">제거할 Azure Attestation에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="80ba8-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="80ba8-125">-ResourceId</span></span>
<span data-ttu-id="80ba8-126">리소스 ID를 토의합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-126">Attestation Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="80ba8-127">-확인</span><span class="sxs-lookup"><span data-stu-id="80ba8-127">-Confirm</span></span>
<span data-ttu-id="80ba8-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="80ba8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="80ba8-129">-WhatIf</span></span>
<span data-ttu-id="80ba8-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="80ba8-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="80ba8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="80ba8-132">CommonParameters</span></span>
<span data-ttu-id="80ba8-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="80ba8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="80ba8-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="80ba8-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="80ba8-135">입력</span><span class="sxs-lookup"><span data-stu-id="80ba8-135">INPUTS</span></span>

### <span data-ttu-id="80ba8-136">System.String</span><span class="sxs-lookup"><span data-stu-id="80ba8-136">System.String</span></span>

### <span data-ttu-id="80ba8-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="80ba8-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="80ba8-138">출력</span><span class="sxs-lookup"><span data-stu-id="80ba8-138">OUTPUTS</span></span>

### <span data-ttu-id="80ba8-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="80ba8-139">System.Boolean</span></span>

## <span data-ttu-id="80ba8-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="80ba8-140">NOTES</span></span>

## <span data-ttu-id="80ba8-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="80ba8-141">RELATED LINKS</span></span>
