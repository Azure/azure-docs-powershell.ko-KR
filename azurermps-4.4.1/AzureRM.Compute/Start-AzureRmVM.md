---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7B3259CD-079D-4E07-8608-F818522EE7CF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVM.md
ms.openlocfilehash: 3091cb877ff792527cf97e3d44b7c363f9dd94b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527707"
---
# <span data-ttu-id="0ed05-101">Start-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-101">Start-AzureRmVM</span></span>

## <span data-ttu-id="0ed05-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0ed05-102">SYNOPSIS</span></span>
<span data-ttu-id="0ed05-103">Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-103">Starts an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0ed05-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0ed05-104">SYNTAX</span></span>

### <span data-ttu-id="0ed05-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="0ed05-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Start-AzureRmVM [-Name] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0ed05-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="0ed05-106">IdParameterSetName</span></span>
```
Start-AzureRmVM [-Name] <String> [-Id] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0ed05-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0ed05-107">DESCRIPTION</span></span>
<span data-ttu-id="0ed05-108">**AzureRmVM** Cmdlet은 Azure 가상 머신을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-108">The **Start-AzureRmVM** cmdlet starts an Azure virtual machine.</span></span>

## <span data-ttu-id="0ed05-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0ed05-109">EXAMPLES</span></span>

### <span data-ttu-id="0ed05-110">예제 1: 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="0ed05-110">Example 1: Start a virtual machine</span></span>
```
PS C:\> Start-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="0ed05-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-111">This command starts the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="0ed05-112">변수</span><span class="sxs-lookup"><span data-stu-id="0ed05-112">PARAMETERS</span></span>

### <span data-ttu-id="0ed05-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0ed05-113">-DefaultProfile</span></span>
<span data-ttu-id="0ed05-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0ed05-115">-Id</span><span class="sxs-lookup"><span data-stu-id="0ed05-115">-Id</span></span>
<span data-ttu-id="0ed05-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-116">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed05-117">-이름</span><span class="sxs-lookup"><span data-stu-id="0ed05-117">-Name</span></span>
<span data-ttu-id="0ed05-118">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-118">The virtual machine name.</span></span>

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

### <span data-ttu-id="0ed05-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0ed05-119">-ResourceGroupName</span></span>
<span data-ttu-id="0ed05-120">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceGroupNameParameterSetName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0ed05-121">-확인</span><span class="sxs-lookup"><span data-stu-id="0ed05-121">-Confirm</span></span>
<span data-ttu-id="0ed05-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0ed05-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0ed05-123">-WhatIf</span></span>
<span data-ttu-id="0ed05-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0ed05-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0ed05-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0ed05-126">CommonParameters</span></span>
<span data-ttu-id="0ed05-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0ed05-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0ed05-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0ed05-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0ed05-129">입력</span><span class="sxs-lookup"><span data-stu-id="0ed05-129">INPUTS</span></span>

## <span data-ttu-id="0ed05-130">출력</span><span class="sxs-lookup"><span data-stu-id="0ed05-130">OUTPUTS</span></span>

## <span data-ttu-id="0ed05-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0ed05-131">NOTES</span></span>

## <span data-ttu-id="0ed05-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0ed05-132">RELATED LINKS</span></span>

[<span data-ttu-id="0ed05-133">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-133">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="0ed05-134">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-134">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="0ed05-135">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-135">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="0ed05-136">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-136">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="0ed05-137">중지-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-137">Stop-AzureRmVM</span></span>](./Stop-AzureRmVM.md)

[<span data-ttu-id="0ed05-138">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="0ed05-138">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


