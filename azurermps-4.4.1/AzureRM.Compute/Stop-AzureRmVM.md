---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7C3CF963-6F1A-444C-B90C-C1D24F89204D
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Stop-AzureRmVM.md
ms.openlocfilehash: f0d6ab84e457894b3c1ff7309efc6914350a03e4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532312"
---
# <span data-ttu-id="06651-101">Stop-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-101">Stop-AzureRmVM</span></span>

## <span data-ttu-id="06651-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06651-102">SYNOPSIS</span></span>
<span data-ttu-id="06651-103">Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-103">Stops an Azure virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="06651-104">구문과</span><span class="sxs-lookup"><span data-stu-id="06651-104">SYNTAX</span></span>

### <span data-ttu-id="06651-105">ResourceGroupNameParameterSetName (기본값)</span><span class="sxs-lookup"><span data-stu-id="06651-105">ResourceGroupNameParameterSetName (Default)</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="06651-106">IdParameterSetName</span><span class="sxs-lookup"><span data-stu-id="06651-106">IdParameterSetName</span></span>
```
Stop-AzureRmVM [-Name] <String> [-Force] [-StayProvisioned] [-Id] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="06651-107">설명은</span><span class="sxs-lookup"><span data-stu-id="06651-107">DESCRIPTION</span></span>
<span data-ttu-id="06651-108">**AzureRmVM** Cmdlet은 Azure 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-108">The **Stop-AzureRmVM** cmdlet stops an Azure virtual machine.</span></span>

## <span data-ttu-id="06651-109">예제의</span><span class="sxs-lookup"><span data-stu-id="06651-109">EXAMPLES</span></span>

### <span data-ttu-id="06651-110">예제 1: 가상 컴퓨터 중지</span><span class="sxs-lookup"><span data-stu-id="06651-110">Example 1: Stop a virtual machine</span></span>
```
PS C:\> Stop-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
```

<span data-ttu-id="06651-111">이 명령은 ResourceGroup11에서 VirtualMachine07 이라는 가상 컴퓨터를 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-111">This command stops the virtual machine named VirtualMachine07 in ResourceGroup11.</span></span>

## <span data-ttu-id="06651-112">변수</span><span class="sxs-lookup"><span data-stu-id="06651-112">PARAMETERS</span></span>

### <span data-ttu-id="06651-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06651-113">-DefaultProfile</span></span>
<span data-ttu-id="06651-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="06651-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06651-115">-Force</span><span class="sxs-lookup"><span data-stu-id="06651-115">-Force</span></span>
<span data-ttu-id="06651-116">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="06651-117">-Id</span><span class="sxs-lookup"><span data-stu-id="06651-117">-Id</span></span>
<span data-ttu-id="06651-118">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06651-118">The resource group name.</span></span>

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

### <span data-ttu-id="06651-119">-이름</span><span class="sxs-lookup"><span data-stu-id="06651-119">-Name</span></span>
<span data-ttu-id="06651-120">가상 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="06651-120">The virtual machine name.</span></span>

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

### <span data-ttu-id="06651-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="06651-121">-ResourceGroupName</span></span>
<span data-ttu-id="06651-122">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="06651-123">-StayProvisioned</span><span class="sxs-lookup"><span data-stu-id="06651-123">-StayProvisioned</span></span>
<span data-ttu-id="06651-124">Cmdlet은 VMSS 내의 모든 가상 컴퓨터를 중지 하지만 할당을 취소 하지는 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06651-124">The cmdlet stops all the virtual machines within the VMSS but does not deallocate them.</span></span> <span data-ttu-id="06651-125">중지 된 가상 컴퓨터에 대해 계정이 청구 됩니다.</span><span class="sxs-lookup"><span data-stu-id="06651-125">The account is charged for the stopped virtual machines.</span></span>

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

### <span data-ttu-id="06651-126">-확인</span><span class="sxs-lookup"><span data-stu-id="06651-126">-Confirm</span></span>
<span data-ttu-id="06651-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="06651-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="06651-128">-WhatIf</span></span>
<span data-ttu-id="06651-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="06651-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="06651-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="06651-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="06651-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06651-131">CommonParameters</span></span>
<span data-ttu-id="06651-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="06651-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06651-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06651-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06651-134">입력</span><span class="sxs-lookup"><span data-stu-id="06651-134">INPUTS</span></span>

## <span data-ttu-id="06651-135">출력</span><span class="sxs-lookup"><span data-stu-id="06651-135">OUTPUTS</span></span>

## <span data-ttu-id="06651-136">상속자</span><span class="sxs-lookup"><span data-stu-id="06651-136">NOTES</span></span>

## <span data-ttu-id="06651-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="06651-137">RELATED LINKS</span></span>

[<span data-ttu-id="06651-138">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-138">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="06651-139">새로운 AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-139">New-AzureRmVM</span></span>](./New-AzureRmVM.md)

[<span data-ttu-id="06651-140">제거-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-140">Remove-AzureRmVM</span></span>](./Remove-AzureRmVM.md)

[<span data-ttu-id="06651-141">다시 시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-141">Restart-AzureRmVM</span></span>](./Restart-AzureRmVM.md)

[<span data-ttu-id="06651-142">시작-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-142">Start-AzureRmVM</span></span>](./Start-AzureRmVM.md)

[<span data-ttu-id="06651-143">업데이트-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="06651-143">Update-AzureRmVM</span></span>](./Update-AzureRmVM.md)


