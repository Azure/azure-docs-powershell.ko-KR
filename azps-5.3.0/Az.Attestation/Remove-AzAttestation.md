---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381102"
---
# <span data-ttu-id="a6a66-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="a6a66-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="a6a66-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a66-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a66-103">Attestation을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-103">Deletes an attestation.</span></span>

## <span data-ttu-id="a6a66-104">구문</span><span class="sxs-lookup"><span data-stu-id="a6a66-104">SYNTAX</span></span>

### <span data-ttu-id="a6a66-105">ByAvailableAttestation(기본값)</span><span class="sxs-lookup"><span data-stu-id="a6a66-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a66-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="a6a66-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a6a66-107">InputObjectByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="a6a66-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a66-108">설명</span><span class="sxs-lookup"><span data-stu-id="a6a66-108">DESCRIPTION</span></span>
<span data-ttu-id="a6a66-109">이 Remove-AzAttestation cmdlet은 지정된 사용 내시를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="a6a66-110">예제</span><span class="sxs-lookup"><span data-stu-id="a6a66-110">EXAMPLES</span></span>

### <span data-ttu-id="a6a66-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a6a66-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="a6a66-112">현재 구독에서 *psh-test-rg라는* 리소스 그룹에서 *pshtest3이라는* 명명된 테스트 공급자를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="a6a66-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6a66-113">PARAMETERS</span></span>

### <span data-ttu-id="a6a66-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a66-114">-DefaultProfile</span></span>
<span data-ttu-id="a6a66-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a6a66-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a6a66-116">-InputObject</span></span>
<span data-ttu-id="a6a66-117">삭제할 Attestation 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="a6a66-118">-Name</span><span class="sxs-lookup"><span data-stu-id="a6a66-118">-Name</span></span>
<span data-ttu-id="a6a66-119">제거할 명세서의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="a6a66-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a6a66-120">-PassThru</span></span>
<span data-ttu-id="a6a66-121">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a6a66-122">이 스위치를 지정하면 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a6a66-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a66-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6a66-124">제거할 Azure 자료에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="a6a66-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a6a66-125">-ResourceId</span></span>
<span data-ttu-id="a6a66-126">Attestation 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="a6a66-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a6a66-127">-Confirm</span></span>
<span data-ttu-id="a6a66-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a6a66-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a66-129">-WhatIf</span></span>
<span data-ttu-id="a6a66-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a6a66-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a6a66-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a6a66-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a66-132">CommonParameters</span></span>
<span data-ttu-id="a6a66-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a66-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a66-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a6a66-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a66-135">입력</span><span class="sxs-lookup"><span data-stu-id="a6a66-135">INPUTS</span></span>

### <span data-ttu-id="a6a66-136">System.String</span><span class="sxs-lookup"><span data-stu-id="a6a66-136">System.String</span></span>

### <span data-ttu-id="a6a66-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span><span class="sxs-lookup"><span data-stu-id="a6a66-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="a6a66-138">출력</span><span class="sxs-lookup"><span data-stu-id="a6a66-138">OUTPUTS</span></span>

### <span data-ttu-id="a6a66-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a6a66-139">System.Boolean</span></span>

## <span data-ttu-id="a6a66-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a6a66-140">NOTES</span></span>

## <span data-ttu-id="a6a66-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a66-141">RELATED LINKS</span></span>
