---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326514"
---
# <span data-ttu-id="b866c-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b866c-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="b866c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b866c-102">SYNOPSIS</span></span>
<span data-ttu-id="b866c-103">컨테이너 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-103">Removes a container service.</span></span>

## <span data-ttu-id="b866c-104">구문</span><span class="sxs-lookup"><span data-stu-id="b866c-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b866c-105">설명</span><span class="sxs-lookup"><span data-stu-id="b866c-105">DESCRIPTION</span></span>
<span data-ttu-id="b866c-106">**Remove-AzContainerService** cmdlet은 Azure 계정에서 컨테이너 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="b866c-107">예제</span><span class="sxs-lookup"><span data-stu-id="b866c-107">EXAMPLES</span></span>

### <span data-ttu-id="b866c-108">예제 1: 컨테이너 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="b866c-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="b866c-109">이 명령은 CSResourceGroup17이라는 컨테이너 서비스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="b866c-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b866c-110">PARAMETERS</span></span>

### <span data-ttu-id="b866c-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b866c-111">-AsJob</span></span>
<span data-ttu-id="b866c-112">백그라운드에서 cmdlet을 실행하고 작업을 반환하여 진행률을 추적합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="b866c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b866c-113">-DefaultProfile</span></span>
<span data-ttu-id="b866c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b866c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="b866c-115">-Force</span></span>
<span data-ttu-id="b866c-116">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b866c-117">-Name</span><span class="sxs-lookup"><span data-stu-id="b866c-117">-Name</span></span>
<span data-ttu-id="b866c-118">이 cmdlet이 제거하는 컨테이너 서비스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b866c-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b866c-119">-ResourceGroupName</span></span>
<span data-ttu-id="b866c-120">이 cmdlet이 제거하는 컨테이너 서비스의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b866c-121">-Confirm</span><span class="sxs-lookup"><span data-stu-id="b866c-121">-Confirm</span></span>
<span data-ttu-id="b866c-122">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b866c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b866c-123">-WhatIf</span></span>
<span data-ttu-id="b866c-124">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="b866c-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b866c-125">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b866c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b866c-126">CommonParameters</span></span>
<span data-ttu-id="b866c-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b866c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b866c-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b866c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b866c-129">입력</span><span class="sxs-lookup"><span data-stu-id="b866c-129">INPUTS</span></span>

### <span data-ttu-id="b866c-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b866c-130">System.String</span></span>

## <span data-ttu-id="b866c-131">출력</span><span class="sxs-lookup"><span data-stu-id="b866c-131">OUTPUTS</span></span>

### <span data-ttu-id="b866c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="b866c-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="b866c-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b866c-133">NOTES</span></span>

## <span data-ttu-id="b866c-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b866c-134">RELATED LINKS</span></span>

[<span data-ttu-id="b866c-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b866c-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="b866c-136">New-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b866c-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="b866c-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="b866c-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


