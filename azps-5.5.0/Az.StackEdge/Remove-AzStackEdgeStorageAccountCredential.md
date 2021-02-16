---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100183217"
---
# <span data-ttu-id="1ff9c-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1ff9c-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1ff9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1ff9c-102">SYNOPSIS</span></span>
<span data-ttu-id="1ff9c-103">디바이스에 대한 저장소 계정 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="1ff9c-104">구문</span><span class="sxs-lookup"><span data-stu-id="1ff9c-104">SYNTAX</span></span>

### <span data-ttu-id="1ff9c-105">DeleteByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="1ff9c-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="1ff9c-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ff9c-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1ff9c-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="1ff9c-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1ff9c-108">설명</span><span class="sxs-lookup"><span data-stu-id="1ff9c-108">DESCRIPTION</span></span>
<span data-ttu-id="1ff9c-109">**Remove-AzStackEdgeStorageAccountCredential** cmdlet은 Stack Edge 디바이스에 대한 저장소 계정 자격 증명을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="1ff9c-110">예제</span><span class="sxs-lookup"><span data-stu-id="1ff9c-110">EXAMPLES</span></span>

### <span data-ttu-id="1ff9c-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1ff9c-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="1ff9c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1ff9c-112">PARAMETERS</span></span>

### <span data-ttu-id="1ff9c-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="1ff9c-113">-AsJob</span></span>
<span data-ttu-id="1ff9c-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="1ff9c-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="1ff9c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1ff9c-115">-DefaultProfile</span></span>
<span data-ttu-id="1ff9c-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1ff9c-117">-DeviceName</span><span class="sxs-lookup"><span data-stu-id="1ff9c-117">-DeviceName</span></span>
<span data-ttu-id="1ff9c-118">디바이스 이름</span><span class="sxs-lookup"><span data-stu-id="1ff9c-118">Device Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff9c-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1ff9c-119">-InputObject</span></span>
<span data-ttu-id="1ff9c-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="1ff9c-120">Input Object</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential
Parameter Sets: DeleteByInputObjectParameterSet
Aliases: StorageAccountCredential

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff9c-121">-Name</span><span class="sxs-lookup"><span data-stu-id="1ff9c-121">-Name</span></span>
<span data-ttu-id="1ff9c-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="1ff9c-122">Name of the storage account to be used</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases: StorageAccountCredentialName

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff9c-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1ff9c-123">-PassThru</span></span>
<span data-ttu-id="1ff9c-124">성공한 경우 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-124">returns true if successful</span></span>

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

### <span data-ttu-id="1ff9c-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1ff9c-125">-ResourceGroupName</span></span>
<span data-ttu-id="1ff9c-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="1ff9c-126">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1ff9c-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ff9c-127">-ResourceId</span></span>
<span data-ttu-id="1ff9c-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="1ff9c-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="1ff9c-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="1ff9c-129">-Confirm</span></span>
<span data-ttu-id="1ff9c-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1ff9c-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1ff9c-131">-WhatIf</span></span>
<span data-ttu-id="1ff9c-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="1ff9c-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1ff9c-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1ff9c-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1ff9c-134">CommonParameters</span></span>
<span data-ttu-id="1ff9c-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1ff9c-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="1ff9c-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1ff9c-137">입력</span><span class="sxs-lookup"><span data-stu-id="1ff9c-137">INPUTS</span></span>

### <span data-ttu-id="1ff9c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="1ff9c-138">System.String</span></span>

### <span data-ttu-id="1ff9c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="1ff9c-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="1ff9c-140">출력</span><span class="sxs-lookup"><span data-stu-id="1ff9c-140">OUTPUTS</span></span>

### <span data-ttu-id="1ff9c-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="1ff9c-141">System.Boolean</span></span>

## <span data-ttu-id="1ff9c-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1ff9c-142">NOTES</span></span>

## <span data-ttu-id="1ff9c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1ff9c-143">RELATED LINKS</span></span>
