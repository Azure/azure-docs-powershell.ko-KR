---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056532"
---
# <span data-ttu-id="5ca70-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ca70-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="5ca70-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5ca70-102">SYNOPSIS</span></span>
<span data-ttu-id="5ca70-103">컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-103">Removes a container service.</span></span>

## <span data-ttu-id="5ca70-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5ca70-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5ca70-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5ca70-105">DESCRIPTION</span></span>
<span data-ttu-id="5ca70-106">**AzContainerService** Cmdlet은 Azure 계정에서 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="5ca70-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5ca70-107">EXAMPLES</span></span>

### <span data-ttu-id="5ca70-108">예제 1: 컨테이너 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="5ca70-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="5ca70-109">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="5ca70-110">변수</span><span class="sxs-lookup"><span data-stu-id="5ca70-110">PARAMETERS</span></span>

### <span data-ttu-id="5ca70-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="5ca70-111">-AsJob</span></span>
<span data-ttu-id="5ca70-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="5ca70-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ca70-113">-DefaultProfile</span></span>
<span data-ttu-id="5ca70-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5ca70-115">-Force</span><span class="sxs-lookup"><span data-stu-id="5ca70-115">-Force</span></span>
<span data-ttu-id="5ca70-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5ca70-117">-이름</span><span class="sxs-lookup"><span data-stu-id="5ca70-117">-Name</span></span>
<span data-ttu-id="5ca70-118">이 cmdlet이 제거 하는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ca70-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ca70-119">-ResourceGroupName</span></span>
<span data-ttu-id="5ca70-120">이 cmdlet이 제거 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="5ca70-121">-확인</span><span class="sxs-lookup"><span data-stu-id="5ca70-121">-Confirm</span></span>
<span data-ttu-id="5ca70-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ca70-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ca70-123">-WhatIf</span></span>
<span data-ttu-id="5ca70-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="5ca70-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ca70-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ca70-126">CommonParameters</span></span>
<span data-ttu-id="5ca70-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5ca70-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ca70-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5ca70-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ca70-129">입력</span><span class="sxs-lookup"><span data-stu-id="5ca70-129">INPUTS</span></span>

### <span data-ttu-id="5ca70-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5ca70-130">System.String</span></span>

## <span data-ttu-id="5ca70-131">출력</span><span class="sxs-lookup"><span data-stu-id="5ca70-131">OUTPUTS</span></span>

### <span data-ttu-id="5ca70-132">PSOperationStatusResponse의. m a.</span><span class="sxs-lookup"><span data-stu-id="5ca70-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="5ca70-133">상속자</span><span class="sxs-lookup"><span data-stu-id="5ca70-133">NOTES</span></span>

## <span data-ttu-id="5ca70-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5ca70-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ca70-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ca70-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="5ca70-136">새로운 AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ca70-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="5ca70-137">업데이트-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="5ca70-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


