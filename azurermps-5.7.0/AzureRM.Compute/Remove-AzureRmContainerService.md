---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526940"
---
# <span data-ttu-id="68ed9-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68ed9-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="68ed9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="68ed9-102">SYNOPSIS</span></span>
<span data-ttu-id="68ed9-103">컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="68ed9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="68ed9-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="68ed9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="68ed9-105">DESCRIPTION</span></span>
<span data-ttu-id="68ed9-106">**AzureRmContainerService** Cmdlet은 Azure 계정에서 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="68ed9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="68ed9-107">EXAMPLES</span></span>

### <span data-ttu-id="68ed9-108">예제 1: 컨테이너 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="68ed9-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="68ed9-109">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="68ed9-110">변수</span><span class="sxs-lookup"><span data-stu-id="68ed9-110">PARAMETERS</span></span>

### <span data-ttu-id="68ed9-111">-Force</span><span class="sxs-lookup"><span data-stu-id="68ed9-111">-Force</span></span>
<span data-ttu-id="68ed9-112">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ed9-113">-이름</span><span class="sxs-lookup"><span data-stu-id="68ed9-113">-Name</span></span>
<span data-ttu-id="68ed9-114">이 cmdlet이 제거 하는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ed9-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="68ed9-115">-ResourceGroupName</span></span>
<span data-ttu-id="68ed9-116">이 cmdlet이 제거 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="68ed9-117">-확인</span><span class="sxs-lookup"><span data-stu-id="68ed9-117">-Confirm</span></span>
<span data-ttu-id="68ed9-118">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ed9-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="68ed9-119">-WhatIf</span></span>
<span data-ttu-id="68ed9-120">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="68ed9-121">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="68ed9-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="68ed9-122">CommonParameters</span></span>
<span data-ttu-id="68ed9-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="68ed9-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="68ed9-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="68ed9-125">입력</span><span class="sxs-lookup"><span data-stu-id="68ed9-125">INPUTS</span></span>

### <span data-ttu-id="68ed9-126">않아야</span><span class="sxs-lookup"><span data-stu-id="68ed9-126">None</span></span>
<span data-ttu-id="68ed9-127">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="68ed9-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="68ed9-128">출력</span><span class="sxs-lookup"><span data-stu-id="68ed9-128">OUTPUTS</span></span>

## <span data-ttu-id="68ed9-129">상속자</span><span class="sxs-lookup"><span data-stu-id="68ed9-129">NOTES</span></span>

## <span data-ttu-id="68ed9-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="68ed9-130">RELATED LINKS</span></span>

[<span data-ttu-id="68ed9-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68ed9-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="68ed9-132">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68ed9-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="68ed9-133">업데이트-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="68ed9-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


