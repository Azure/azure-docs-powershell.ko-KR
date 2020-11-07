---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 7F7D1F05-617C-4EC5-8FF5-D816E9148841
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Start-AzureRmVmss.md
ms.openlocfilehash: 6b3291a77f7c69372124b8c0de2ba78c8810f02b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703128"
---
# <span data-ttu-id="ed6f4-101">Start-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-101">Start-AzureRmVmss</span></span>

## <span data-ttu-id="ed6f4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ed6f4-102">SYNOPSIS</span></span>
<span data-ttu-id="ed6f4-103">Vmss 또는 VMSS 내의 가상 컴퓨터 집합을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-103">Starts the VMSS or a set of virtual machines within the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ed6f4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ed6f4-104">SYNTAX</span></span>

```
Start-AzureRmVmss [-ResourceGroupName] <String> [-VMScaleSetName] <String> [[-InstanceId] <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ed6f4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ed6f4-105">DESCRIPTION</span></span>
<span data-ttu-id="ed6f4-106">**AzureRmVmss** CMDLET은 vmss (가상 컴퓨터 크기 집합) 또는 가상 컴퓨터 집합 내의 모든 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-106">The **Start-AzureRmVmss** cmdlet starts all the virtual machines within the Virtual Machine Scale Set (VMSS) or a set of virtual machines.</span></span>
<span data-ttu-id="ed6f4-107">*InstanceId* 매개 변수를 사용 하 여 가상 컴퓨터 집합을 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-107">You can use the *InstanceId* parameter to select a set of virtual machines.</span></span>

## <span data-ttu-id="ed6f4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="ed6f4-108">EXAMPLES</span></span>

### <span data-ttu-id="ed6f4-109">예제 1: VMSS 내에서 가상 컴퓨터의 특정 집합 시작</span><span class="sxs-lookup"><span data-stu-id="ed6f4-109">Example 1: Start a specific set of virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"-InstanceId "0", "1"
```

<span data-ttu-id="ed6f4-110">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 인스턴스 ID 문자열 배열에 지정 된 가상 컴퓨터의 특정 집합을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-110">This command starts a specific set of virtual machines specified by the instance ID string array that belong to the VMSS named ContosoVMSS.</span></span>

### <span data-ttu-id="ed6f4-111">예제 2: VMSS 내의 모든 가상 컴퓨터 시작</span><span class="sxs-lookup"><span data-stu-id="ed6f4-111">Example 2: Start all virtual machines within the VMSS</span></span>
```
PS C:\> Start-AzureRmVmss -ResourceGroupName "ContosOrg" -VMScaleSetName "ContosoVMSS"
```

<span data-ttu-id="ed6f4-112">이 명령은 ContosoVMSS 이라는 VMSS에 속하는 모든 가상 컴퓨터를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-112">This command starts all virtual machines that belong to the VMSS named ContosoVMSS.</span></span>

## <span data-ttu-id="ed6f4-113">변수</span><span class="sxs-lookup"><span data-stu-id="ed6f4-113">PARAMETERS</span></span>

### <span data-ttu-id="ed6f4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ed6f4-114">-DefaultProfile</span></span>
<span data-ttu-id="ed6f4-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ed6f4-116">-InstanceId</span><span class="sxs-lookup"><span data-stu-id="ed6f4-116">-InstanceId</span></span>
<span data-ttu-id="ed6f4-117">Cmdlet이 시작 되는 인스턴스의 ID 또는 식별자를 문자열 배열로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-117">Specifies, as a string array, the ID or IDs of the instances that cmdlet starts.</span></span>
<span data-ttu-id="ed6f4-118">예를 들면 다음과 같습니다. `-InstanceId "0", "3"`</span><span class="sxs-lookup"><span data-stu-id="ed6f4-118">For instance: `-InstanceId "0", "3"`</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6f4-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ed6f4-119">-ResourceGroupName</span></span>
<span data-ttu-id="ed6f4-120">VMSS의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-120">Specifies the name of the resource group of the VMSS.</span></span>

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

### <span data-ttu-id="ed6f4-121">-VMScaleSetName</span><span class="sxs-lookup"><span data-stu-id="ed6f4-121">-VMScaleSetName</span></span>
<span data-ttu-id="ed6f4-122">이 cmdlet이 가상 컴퓨터를 시작 하는 VMSS의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-122">Specifies the name of the VMSS that this cmdlet starts the virtual machines.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ed6f4-123">-확인</span><span class="sxs-lookup"><span data-stu-id="ed6f4-123">-Confirm</span></span>
<span data-ttu-id="ed6f4-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ed6f4-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ed6f4-125">-WhatIf</span></span>
<span data-ttu-id="ed6f4-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ed6f4-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ed6f4-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ed6f4-128">CommonParameters</span></span>
<span data-ttu-id="ed6f4-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ed6f4-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ed6f4-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ed6f4-131">입력</span><span class="sxs-lookup"><span data-stu-id="ed6f4-131">INPUTS</span></span>

## <span data-ttu-id="ed6f4-132">출력</span><span class="sxs-lookup"><span data-stu-id="ed6f4-132">OUTPUTS</span></span>

###  
<span data-ttu-id="ed6f4-133">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ed6f4-133">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="ed6f4-134">상속자</span><span class="sxs-lookup"><span data-stu-id="ed6f4-134">NOTES</span></span>

## <span data-ttu-id="ed6f4-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ed6f4-135">RELATED LINKS</span></span>

[<span data-ttu-id="ed6f4-136">Get-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-136">Get-AzureRmVmss</span></span>](./Get-AzureRmVmss.md)

[<span data-ttu-id="ed6f4-137">새로운 AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-137">New-AzureRmVmss</span></span>](./New-AzureRmVmss.md)

[<span data-ttu-id="ed6f4-138">제거-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-138">Remove-AzureRmVmss</span></span>](./Remove-AzureRmVmss.md)

[<span data-ttu-id="ed6f4-139">다시 시작-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-139">Restart-AzureRmVmss</span></span>](./Restart-AzureRmVmss.md)

[<span data-ttu-id="ed6f4-140">Set-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-140">Set-AzureRmVmss</span></span>](./Set-AzureRmVmss.md)

[<span data-ttu-id="ed6f4-141">중지-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-141">Stop-AzureRmVmss</span></span>](./Stop-AzureRmVmss.md)

[<span data-ttu-id="ed6f4-142">업데이트-AzureRmVmss</span><span class="sxs-lookup"><span data-stu-id="ed6f4-142">Update-AzureRmVmss</span></span>](./Update-AzureRmVmss.md)


