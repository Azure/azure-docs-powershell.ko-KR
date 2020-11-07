---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Attestation.dll-Help.xml
Module Name: Az.Attestation
online version: https://docs.microsoft.com/en-us/powershell/module/az.attestation/remove-azattestation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Attestation/Attestation/help/Remove-AzAttestation.md
ms.openlocfilehash: 997e1150549ac219c54e42fdd4c7674cd53d5ddc
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697882"
---
# <span data-ttu-id="5a93a-101">Remove-AzAttestation</span><span class="sxs-lookup"><span data-stu-id="5a93a-101">Remove-AzAttestation</span></span>

## <span data-ttu-id="5a93a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a93a-102">SYNOPSIS</span></span>
<span data-ttu-id="5a93a-103">증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-103">Deletes an attestation.</span></span>

## <span data-ttu-id="5a93a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5a93a-104">SYNTAX</span></span>

### <span data-ttu-id="5a93a-105">Byon 증명 (기본값)</span><span class="sxs-lookup"><span data-stu-id="5a93a-105">ByAvailableAttestation (Default)</span></span>
```
Remove-AzAttestation [-Name] <String> [-ResourceGroupName] <String> [-AsJob] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a93a-106">ResourceIdByAvailableAttestation</span><span class="sxs-lookup"><span data-stu-id="5a93a-106">ResourceIdByAvailableAttestation</span></span>
```
Remove-AzAttestation [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5a93a-107">Inputobjectby해당 증명</span><span class="sxs-lookup"><span data-stu-id="5a93a-107">InputObjectByAvailableAttestation</span></span>
```
Remove-AzAttestation [-InputObject] <PSAttestation> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5a93a-108">설명은</span><span class="sxs-lookup"><span data-stu-id="5a93a-108">DESCRIPTION</span></span>
<span data-ttu-id="5a93a-109">Remove-AzAttestation cmdlet은 지정 된 증명을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-109">The Remove-AzAttestation cmdlet deletes the specified attestation.</span></span>

## <span data-ttu-id="5a93a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="5a93a-110">EXAMPLES</span></span>

### <span data-ttu-id="5a93a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="5a93a-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzAttestation -Name example -ResourceGroupName rg1 
```

<span data-ttu-id="5a93a-112">현재 구독 및 리소스 그룹 "rg1"에서 증명 "예제"를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-112">Delete Attestation "example" from current Subscription and Resource Group "rg1".</span></span>

## <span data-ttu-id="5a93a-113">변수</span><span class="sxs-lookup"><span data-stu-id="5a93a-113">PARAMETERS</span></span>

### <span data-ttu-id="5a93a-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5a93a-114">-AsJob</span></span>
<span data-ttu-id="5a93a-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="5a93a-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="5a93a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a93a-116">-DefaultProfile</span></span>
<span data-ttu-id="5a93a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5a93a-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5a93a-118">-InputObject</span></span>
<span data-ttu-id="5a93a-119">삭제할 증명 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-119">Attestation object to be deleted.</span></span>

```yaml
Type: PSAttestation
Parameter Sets: InputObjectByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5a93a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="5a93a-120">-Name</span></span>
<span data-ttu-id="5a93a-121">제거할 증명의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-121">Specifies the name of the attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a93a-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5a93a-122">-PassThru</span></span>
<span data-ttu-id="5a93a-123">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-123">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="5a93a-124">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-124">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="5a93a-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5a93a-125">-ResourceGroupName</span></span>
<span data-ttu-id="5a93a-126">제거할 Azure 증명에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-126">Specifies the name of resource group for Azure attestation to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByAvailableAttestation
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a93a-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="5a93a-127">-ResourceId</span></span>
<span data-ttu-id="5a93a-128">증명 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-128">Attestation Resource Id.</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdByAvailableAttestation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a93a-129">-확인</span><span class="sxs-lookup"><span data-stu-id="5a93a-129">-Confirm</span></span>
<span data-ttu-id="5a93a-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5a93a-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5a93a-131">-WhatIf</span></span>
<span data-ttu-id="5a93a-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5a93a-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5a93a-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a93a-134">CommonParameters</span></span>
<span data-ttu-id="5a93a-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5a93a-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a93a-136">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5a93a-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a93a-137">입력</span><span class="sxs-lookup"><span data-stu-id="5a93a-137">INPUTS</span></span>

### <span data-ttu-id="5a93a-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5a93a-138">System.String</span></span>

### <span data-ttu-id="5a93a-139">Microsoft. Azure. PSAttestation</span><span class="sxs-lookup"><span data-stu-id="5a93a-139">Microsoft.Azure.Commands.Attestation.Models.PSAttestation</span></span>

## <span data-ttu-id="5a93a-140">출력</span><span class="sxs-lookup"><span data-stu-id="5a93a-140">OUTPUTS</span></span>

### <span data-ttu-id="5a93a-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="5a93a-141">System.Boolean</span></span>

## <span data-ttu-id="5a93a-142">상속자</span><span class="sxs-lookup"><span data-stu-id="5a93a-142">NOTES</span></span>

## <span data-ttu-id="5a93a-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5a93a-143">RELATED LINKS</span></span>
