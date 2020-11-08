---
external help file: Microsoft.Azure.PowerShell.Cmdlets.StackEdge.dll-Help.xml
Module Name: Az.StackEdge
online version: https://docs.microsoft.com/en-us/powershell/module/az.stackedge/remove-azstackedgestorageaccountcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/StackEdge/StackEdge/help/Remove-AzStackEdgeStorageAccountCredential.md
ms.openlocfilehash: 1a55a8c08182ae4a32e27bec74e4a5870aae95fa
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213211"
---
# <span data-ttu-id="7419e-101">Remove-AzStackEdgeStorageAccountCredential</span><span class="sxs-lookup"><span data-stu-id="7419e-101">Remove-AzStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7419e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7419e-102">SYNOPSIS</span></span>
<span data-ttu-id="7419e-103">장치에 대 한 저장소 계정 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-103">Removes a storage account credential for a device.</span></span>

## <span data-ttu-id="7419e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7419e-104">SYNTAX</span></span>

### <span data-ttu-id="7419e-105">DeleteByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="7419e-105">DeleteByNameParameterSet (Default)</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceGroupName] <String> [-DeviceName] <String>
 [-Name] <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7419e-106">DeleteByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7419e-106">DeleteByResourceIdParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-ResourceId] <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7419e-107">DeleteByInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7419e-107">DeleteByInputObjectParameterSet</span></span>
```
Remove-AzStackEdgeStorageAccountCredential [-InputObject] <PSStackEdgeStorageAccountCredential> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-PassThru] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7419e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="7419e-108">DESCRIPTION</span></span>
<span data-ttu-id="7419e-109">**AzStackEdgeStorageAccountCredential** Cmdlet은 스택 경계 장치에 대 한 저장소 계정 자격 증명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-109">The **Remove-AzStackEdgeStorageAccountCredential** cmdlet removes the storage account credential for a Stack Edge device.</span></span>

## <span data-ttu-id="7419e-110">예제의</span><span class="sxs-lookup"><span data-stu-id="7419e-110">EXAMPLES</span></span>

### <span data-ttu-id="7419e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7419e-111">Example 1</span></span>
```powershell
PS C:\> Remove-AzStackEdgeStorageAccountCredential ResourceGroupName resourceGroupName -DeviceName deviceName -Name storageAccountCredentialName
```

## <span data-ttu-id="7419e-112">변수</span><span class="sxs-lookup"><span data-stu-id="7419e-112">PARAMETERS</span></span>

### <span data-ttu-id="7419e-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7419e-113">-AsJob</span></span>
<span data-ttu-id="7419e-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="7419e-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="7419e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7419e-115">-DefaultProfile</span></span>
<span data-ttu-id="7419e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7419e-117">-장치 이름</span><span class="sxs-lookup"><span data-stu-id="7419e-117">-DeviceName</span></span>
<span data-ttu-id="7419e-118">장치 이름</span><span class="sxs-lookup"><span data-stu-id="7419e-118">Device Name</span></span>

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

### <span data-ttu-id="7419e-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7419e-119">-InputObject</span></span>
<span data-ttu-id="7419e-120">입력 개체</span><span class="sxs-lookup"><span data-stu-id="7419e-120">Input Object</span></span>

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

### <span data-ttu-id="7419e-121">-이름</span><span class="sxs-lookup"><span data-stu-id="7419e-121">-Name</span></span>
<span data-ttu-id="7419e-122">사용할 저장소 계정의 이름</span><span class="sxs-lookup"><span data-stu-id="7419e-122">Name of the storage account to be used</span></span>

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

### <span data-ttu-id="7419e-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7419e-123">-PassThru</span></span>
<span data-ttu-id="7419e-124">성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-124">returns true if successful</span></span>

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

### <span data-ttu-id="7419e-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7419e-125">-ResourceGroupName</span></span>
<span data-ttu-id="7419e-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="7419e-126">Resource Group Name</span></span>

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

### <span data-ttu-id="7419e-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7419e-127">-ResourceId</span></span>
<span data-ttu-id="7419e-128">Azure ResourceId</span><span class="sxs-lookup"><span data-stu-id="7419e-128">Azure ResourceId</span></span>

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

### <span data-ttu-id="7419e-129">-확인</span><span class="sxs-lookup"><span data-stu-id="7419e-129">-Confirm</span></span>
<span data-ttu-id="7419e-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7419e-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7419e-131">-WhatIf</span></span>
<span data-ttu-id="7419e-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7419e-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7419e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7419e-134">CommonParameters</span></span>
<span data-ttu-id="7419e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7419e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7419e-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7419e-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7419e-137">입력</span><span class="sxs-lookup"><span data-stu-id="7419e-137">INPUTS</span></span>

### <span data-ttu-id="7419e-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="7419e-138">System.String</span></span>

### <span data-ttu-id="7419e-139">StackEdge. PSStackEdgeStorageAccountCredential에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="7419e-139">Microsoft.Azure.PowerShell.Cmdlets.StackEdge.Models.PSStackEdgeStorageAccountCredential</span></span>

## <span data-ttu-id="7419e-140">출력</span><span class="sxs-lookup"><span data-stu-id="7419e-140">OUTPUTS</span></span>

### <span data-ttu-id="7419e-141">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="7419e-141">System.Boolean</span></span>

## <span data-ttu-id="7419e-142">상속자</span><span class="sxs-lookup"><span data-stu-id="7419e-142">NOTES</span></span>

## <span data-ttu-id="7419e-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7419e-143">RELATED LINKS</span></span>
