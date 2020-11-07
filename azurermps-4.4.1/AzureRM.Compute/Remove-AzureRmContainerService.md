---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: fc66151f39c969ebbdc9b54d6f6ed97db909e05b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711285"
---
# <span data-ttu-id="4024b-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4024b-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="4024b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4024b-102">SYNOPSIS</span></span>
<span data-ttu-id="4024b-103">컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4024b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4024b-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4024b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4024b-105">DESCRIPTION</span></span>
<span data-ttu-id="4024b-106">**AzureRmContainerService** Cmdlet은 Azure 계정에서 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="4024b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4024b-107">EXAMPLES</span></span>

### <span data-ttu-id="4024b-108">예제 1: 컨테이너 서비스 제거</span><span class="sxs-lookup"><span data-stu-id="4024b-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="4024b-109">이 명령은 CSResourceGroup17 이라는 컨테이너 서비스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="4024b-110">변수</span><span class="sxs-lookup"><span data-stu-id="4024b-110">PARAMETERS</span></span>

### <span data-ttu-id="4024b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4024b-111">-DefaultProfile</span></span>
<span data-ttu-id="4024b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4024b-113">-Force</span><span class="sxs-lookup"><span data-stu-id="4024b-113">-Force</span></span>
<span data-ttu-id="4024b-114">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="4024b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="4024b-115">-Name</span></span>
<span data-ttu-id="4024b-116">이 cmdlet이 제거 하는 컨테이너 서비스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-116">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4024b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4024b-117">-ResourceGroupName</span></span>
<span data-ttu-id="4024b-118">이 cmdlet이 제거 하는 컨테이너 서비스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-118">Specifies the resource group of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="4024b-119">-확인</span><span class="sxs-lookup"><span data-stu-id="4024b-119">-Confirm</span></span>
<span data-ttu-id="4024b-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-120">Prompts you for confirmation before running the cmdlet.</span></span>
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

### <span data-ttu-id="4024b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4024b-121">-WhatIf</span></span>
<span data-ttu-id="4024b-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4024b-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-123">The cmdlet is not run.</span></span>
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

### <span data-ttu-id="4024b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4024b-124">CommonParameters</span></span>
<span data-ttu-id="4024b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4024b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4024b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4024b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4024b-127">입력</span><span class="sxs-lookup"><span data-stu-id="4024b-127">INPUTS</span></span>

## <span data-ttu-id="4024b-128">출력</span><span class="sxs-lookup"><span data-stu-id="4024b-128">OUTPUTS</span></span>

## <span data-ttu-id="4024b-129">상속자</span><span class="sxs-lookup"><span data-stu-id="4024b-129">NOTES</span></span>

## <span data-ttu-id="4024b-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4024b-130">RELATED LINKS</span></span>

[<span data-ttu-id="4024b-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4024b-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="4024b-132">새로운 AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4024b-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="4024b-133">업데이트-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="4024b-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


