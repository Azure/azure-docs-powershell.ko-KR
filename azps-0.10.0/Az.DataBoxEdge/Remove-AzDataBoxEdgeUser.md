---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.dll-Help.xml
Module Name: Az.DataBoxEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.databoxedge/remove-azdataboxedgeuser
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/DataBoxEdge/DataBoxEdge/help/Remove-AzDataBoxEdgeUser.md
ms.openlocfilehash: 1d6c99a44e2163f2d441dcacc87cf202f334f330
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875969"
---
# <span data-ttu-id="58fbb-101">Remove-AzDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="58fbb-101">Remove-AzDataBoxEdgeUser</span></span>

## <span data-ttu-id="58fbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="58fbb-102">SYNOPSIS</span></span>
<span data-ttu-id="58fbb-103">장치에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-103">Removes a user on a device.</span></span>

## <span data-ttu-id="58fbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="58fbb-104">SYNTAX</span></span>

### <span data-ttu-id="58fbb-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="58fbb-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceGroupName] <String> [-DeviceName] <String> [-Name] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58fbb-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="58fbb-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-ResourceId] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="58fbb-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="58fbb-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzDataBoxEdgeUser [-InputObject] <PSDataBoxEdgeUser> [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="58fbb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="58fbb-108">DESCRIPTION</span></span>
<span data-ttu-id="58fbb-109">**AzDataBoxEdgeUser** Cmdlet은 데이터 상자 가장자리 장치에서 사용자를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-109">The **Remove-AzDataBoxEdgeUser** cmdlet removes a user on the Data Box Edge device.</span></span> <span data-ttu-id="58fbb-110">유형의 사용자 만들기만 `Share` 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-110">Creation of only users of type `Share` is supported.</span></span>

## <span data-ttu-id="58fbb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="58fbb-111">EXAMPLES</span></span>

### <span data-ttu-id="58fbb-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="58fbb-112">Example 1</span></span>
```powershell
PS C:\> Remove-AzDataBoxEdgeUser -ResourceGroupName resourceGroupName -DeviceName deviceName -Name username
```

## <span data-ttu-id="58fbb-113">변수</span><span class="sxs-lookup"><span data-stu-id="58fbb-113">PARAMETERS</span></span>

### <span data-ttu-id="58fbb-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="58fbb-114">-AsJob</span></span>
<span data-ttu-id="58fbb-115">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="58fbb-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="58fbb-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="58fbb-116">-DefaultProfile</span></span>
<span data-ttu-id="58fbb-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="58fbb-118">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="58fbb-118">-DeviceName</span></span>
<span data-ttu-id="58fbb-119">장치 이름</span><span class="sxs-lookup"><span data-stu-id="58fbb-119">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fbb-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="58fbb-120">-InputObject</span></span>
<span data-ttu-id="58fbb-121">입력 개체</span><span class="sxs-lookup"><span data-stu-id="58fbb-121">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser
Parameter Sets: DeleteByInputObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="58fbb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="58fbb-122">-Name</span></span>
<span data-ttu-id="58fbb-123">사용자</span><span class="sxs-lookup"><span data-stu-id="58fbb-123">Username</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fbb-124">-PassThru</span><span class="sxs-lookup"><span data-stu-id="58fbb-124">-PassThru</span></span>
<span data-ttu-id="58fbb-125">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-125">returns true if successful</span></span>

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

### <span data-ttu-id="58fbb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="58fbb-126">-ResourceGroupName</span></span>
<span data-ttu-id="58fbb-127">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="58fbb-127">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="58fbb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="58fbb-128">-ResourceId</span></span>
<span data-ttu-id="58fbb-129">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="58fbb-129">Azure ResourceId</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="58fbb-130">-확인</span><span class="sxs-lookup"><span data-stu-id="58fbb-130">-Confirm</span></span>
<span data-ttu-id="58fbb-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="58fbb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="58fbb-132">-WhatIf</span></span>
<span data-ttu-id="58fbb-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="58fbb-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="58fbb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="58fbb-135">CommonParameters</span></span>
<span data-ttu-id="58fbb-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="58fbb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="58fbb-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="58fbb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="58fbb-138">입력</span><span class="sxs-lookup"><span data-stu-id="58fbb-138">INPUTS</span></span>

### <span data-ttu-id="58fbb-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="58fbb-139">System.String</span></span>

### <span data-ttu-id="58fbb-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span><span class="sxs-lookup"><span data-stu-id="58fbb-140">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeUser</span></span>

## <span data-ttu-id="58fbb-141">출력</span><span class="sxs-lookup"><span data-stu-id="58fbb-141">OUTPUTS</span></span>

### <span data-ttu-id="58fbb-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="58fbb-142">Microsoft.Azure.PowerShell.Cmdlets.DataBoxEdge.Models.PSDataBoxEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="58fbb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="58fbb-143">NOTES</span></span>

## <span data-ttu-id="58fbb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="58fbb-144">RELATED LINKS</span></span>
