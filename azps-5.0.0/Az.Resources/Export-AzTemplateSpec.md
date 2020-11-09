---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: 9b0db1cc72064b502b9961fba73598b94790af1a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308333"
---
# <span data-ttu-id="074c5-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="074c5-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="074c5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="074c5-102">SYNOPSIS</span></span>
<span data-ttu-id="074c5-103">템플릿 사양을 로컬 파일 시스템으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="074c5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="074c5-104">SYNTAX</span></span>

### <span data-ttu-id="074c5-105">ExportByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="074c5-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="074c5-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="074c5-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="074c5-107">설명은</span><span class="sxs-lookup"><span data-stu-id="074c5-107">DESCRIPTION</span></span>
<span data-ttu-id="074c5-108">특정 템플릿 사양 버전을 로컬 파일 시스템으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="074c5-109">예제의</span><span class="sxs-lookup"><span data-stu-id="074c5-109">EXAMPLES</span></span>

### <span data-ttu-id="074c5-110">예제 1: 이름으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="074c5-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="074c5-111">리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전을 로컬 출력 폴더 "v1"으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="074c5-112">예제 2: 리소스 id를 기준으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="074c5-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="074c5-113">구독 하위 id의 ' myRG ' 리소스 그룹에 있는 ' MyTemplateSpec ' 템플릿 사양의 ' v 1.0 ' 버전 \{ \} 을 로컬 출력 폴더 "v1"으로 내보냅니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="074c5-114">변수</span><span class="sxs-lookup"><span data-stu-id="074c5-114">PARAMETERS</span></span>

### <span data-ttu-id="074c5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="074c5-115">-DefaultProfile</span></span>
<span data-ttu-id="074c5-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="074c5-117">-이름</span><span class="sxs-lookup"><span data-stu-id="074c5-117">-Name</span></span>
<span data-ttu-id="074c5-118">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="074c5-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="074c5-119">-OutputFolder</span></span>
<span data-ttu-id="074c5-120">템플릿 사양 버전이 출력 되는 폴더의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-120">The path to the folder where the template spec version will be output to.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="074c5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="074c5-121">-ResourceGroupName</span></span>
<span data-ttu-id="074c5-122">템플릿 사양의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="074c5-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="074c5-123">-ResourceId</span></span>
<span data-ttu-id="074c5-124">템플릿 사양의 정규화 된 리소스 Id입니다. 예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="074c5-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="074c5-125">-버전</span><span class="sxs-lookup"><span data-stu-id="074c5-125">-Version</span></span>
<span data-ttu-id="074c5-126">내보낼 템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-126">The version of the template spec to export.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="074c5-127">-확인</span><span class="sxs-lookup"><span data-stu-id="074c5-127">-Confirm</span></span>
<span data-ttu-id="074c5-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="074c5-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="074c5-129">-WhatIf</span></span>
<span data-ttu-id="074c5-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="074c5-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="074c5-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="074c5-132">CommonParameters</span></span>
<span data-ttu-id="074c5-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="074c5-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="074c5-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="074c5-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="074c5-135">입력</span><span class="sxs-lookup"><span data-stu-id="074c5-135">INPUTS</span></span>

### <span data-ttu-id="074c5-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="074c5-136">System.String</span></span>

## <span data-ttu-id="074c5-137">출력</span><span class="sxs-lookup"><span data-stu-id="074c5-137">OUTPUTS</span></span>

### <span data-ttu-id="074c5-138">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="074c5-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="074c5-139">상속자</span><span class="sxs-lookup"><span data-stu-id="074c5-139">NOTES</span></span>

## <span data-ttu-id="074c5-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="074c5-140">RELATED LINKS</span></span>
