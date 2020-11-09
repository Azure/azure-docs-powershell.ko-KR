---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 16e728443e228a2a9b85806caf8cf55ec9c115c3
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307598"
---
# <span data-ttu-id="964e2-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="964e2-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="964e2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="964e2-102">SYNOPSIS</span></span>
<span data-ttu-id="964e2-103">증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-103">Deletes an attestation.</span></span>

## <span data-ttu-id="964e2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="964e2-104">SYNTAX</span></span>

### <span data-ttu-id="964e2-105">Byon 증명 (기본값)</span><span class="sxs-lookup"><span data-stu-id="964e2-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="964e2-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="964e2-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="964e2-107">Inputobjectby해당 증명</span><span class="sxs-lookup"><span data-stu-id="964e2-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="964e2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="964e2-108">DESCRIPTION</span></span>
<span data-ttu-id="964e2-109">Remove-AzAttestation cmdlet은 지정 된 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="964e2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="964e2-110">EXAMPLES</span></span>

### <span data-ttu-id="964e2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="964e2-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name pshtest3 -ResourceGroupName psh-test-rg
```

<span data-ttu-id="964e2-112">현재 구독에서 *psh-test-rg* 이라는 리소스 그룹의 *Pshtest3* 이라는 증명 공급자를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-112">Delete the Attestation Provider named *pshtest3* in the resource group named *psh-test-rg* from the current subscription.</span></span>

## <span data-ttu-id="964e2-113">변수</span><span class="sxs-lookup"><span data-stu-id="964e2-113">PARAMETERS</span></span>

### <span data-ttu-id="964e2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="964e2-114">-DefaultProfile</span></span>
<span data-ttu-id="964e2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="964e2-116">-InputObject</span><span class="sxs-lookup"><span data-stu-id="964e2-116">-InputObject</span></span>
<span data-ttu-id="964e2-117">삭제할 증명 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-117">Attestation object to be deleted.</span></span>

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

### <span data-ttu-id="964e2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="964e2-118">-Name</span></span>
<span data-ttu-id="964e2-119">제거할 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-119">Specifies the name of the attestation to remove.</span></span>

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

### <span data-ttu-id="964e2-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="964e2-120">-PassThru</span></span>
<span data-ttu-id="964e2-121">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-121">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="964e2-122">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-122">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="964e2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="964e2-123">-ResourceGroupName</span></span>
<span data-ttu-id="964e2-124">제거할 Azure 증명에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-124">Specifies the name of resource group for Azure attestation to remove.</span></span>

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

### <span data-ttu-id="964e2-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="964e2-125">-ResourceId</span></span>
<span data-ttu-id="964e2-126">증명 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-126">Attestation Resource Id.</span></span>

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

### <span data-ttu-id="964e2-127">-확인</span><span class="sxs-lookup"><span data-stu-id="964e2-127">-Confirm</span></span>
<span data-ttu-id="964e2-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="964e2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="964e2-129">-WhatIf</span></span>
<span data-ttu-id="964e2-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="964e2-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="964e2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="964e2-132">CommonParameters</span></span>
<span data-ttu-id="964e2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="964e2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="964e2-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="964e2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="964e2-135">입력</span><span class="sxs-lookup"><span data-stu-id="964e2-135">INPUTS</span></span>

### <span data-ttu-id="964e2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="964e2-136">System.String</span></span>

### <span data-ttu-id="964e2-137">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="964e2-137">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="964e2-138">출력</span><span class="sxs-lookup"><span data-stu-id="964e2-138">OUTPUTS</span></span>

### <span data-ttu-id="964e2-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="964e2-139">System.Boolean</span></span>

## <span data-ttu-id="964e2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="964e2-140">NOTES</span></span>

## <span data-ttu-id="964e2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="964e2-141">RELATED LINKS</span></span>
