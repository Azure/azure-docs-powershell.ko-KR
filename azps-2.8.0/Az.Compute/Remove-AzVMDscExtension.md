---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: C7FCF2CA-2C8D-4280-BF68-10DEA96642A5
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdscextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDscExtension.md
ms.openlocfilehash: 2fdbafba325d95f8e0ce2959e6f77c896dfa0722
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697293"
---
# <span data-ttu-id="40358-101">Remove-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="40358-101">Remove-AzVMDscExtension</span></span>

## <span data-ttu-id="40358-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40358-102">SYNOPSIS</span></span>
<span data-ttu-id="40358-103">리소스 그룹의 가상 컴퓨터에서 DSC 확장 처리기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-103">Removes a DSC extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="40358-104">구문과</span><span class="sxs-lookup"><span data-stu-id="40358-104">SYNTAX</span></span>

```
Remove-AzVMDscExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-NoWait]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40358-105">설명은</span><span class="sxs-lookup"><span data-stu-id="40358-105">DESCRIPTION</span></span>
<span data-ttu-id="40358-106">**AzVMDscExtension** cmdlet은 리소스 그룹의 가상 컴퓨터에서 원하는 상태 구성 (DSC) 확장 처리기를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-106">The **Remove-AzVMDscExtension** cmdlet removes a Desired State Configuration (DSC) extension handler from a virtual machine in a resource group.</span></span>

## <span data-ttu-id="40358-107">예제의</span><span class="sxs-lookup"><span data-stu-id="40358-107">EXAMPLES</span></span>

### <span data-ttu-id="40358-108">예제 1: DSC 확장 제거</span><span class="sxs-lookup"><span data-stu-id="40358-108">Example 1: Remove a DSC extension</span></span>
```
PS C:\> Remove-AzVMDscExtension -ResourceGroupName "ResourceGroup001" -VMName "VM07" -Name "DSC"
```

<span data-ttu-id="40358-109">이 명령은 VM07 이라는 가상 컴퓨터에서 DSC 라는 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-109">This command removes the extension named DSC on virtual machine named VM07.</span></span>

## <span data-ttu-id="40358-110">변수</span><span class="sxs-lookup"><span data-stu-id="40358-110">PARAMETERS</span></span>

### <span data-ttu-id="40358-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40358-111">-DefaultProfile</span></span>
<span data-ttu-id="40358-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40358-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="40358-113">-이름</span><span class="sxs-lookup"><span data-stu-id="40358-113">-Name</span></span>
<span data-ttu-id="40358-114">이 cmdlet이 제거 하는 DSC 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-114">Specifies the name of the DSC extension that this cmdlet removes.</span></span>
<span data-ttu-id="40358-115">Set-AzVMDscExtension cmdlet은이 이름을 **AzVMDscExtension** 에 사용 되는 기본 값인 Microsoft Powershell로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-115">The Set-AzVMDscExtension cmdlet sets this name to Microsoft.Powershell.DSC, which is the default value used by **Remove-AzVMDscExtension**.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40358-116">-NoWait</span><span class="sxs-lookup"><span data-stu-id="40358-116">-NoWait</span></span>
<span data-ttu-id="40358-117">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-117">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="40358-118">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-118">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="40358-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40358-119">-ResourceGroupName</span></span>
<span data-ttu-id="40358-120">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-120">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="40358-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="40358-121">-VMName</span></span>
<span data-ttu-id="40358-122">이 cmdlet이 DSC 확장을 제거 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-122">Specifies the name of a virtual machine from which this cmdlet removes the DSC extension.</span></span>

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

### <span data-ttu-id="40358-123">-확인</span><span class="sxs-lookup"><span data-stu-id="40358-123">-Confirm</span></span>
<span data-ttu-id="40358-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40358-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40358-125">-WhatIf</span></span>
<span data-ttu-id="40358-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="40358-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="40358-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40358-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40358-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40358-128">CommonParameters</span></span>
<span data-ttu-id="40358-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="40358-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40358-130">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="40358-130">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40358-131">입력</span><span class="sxs-lookup"><span data-stu-id="40358-131">INPUTS</span></span>

### <span data-ttu-id="40358-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="40358-132">System.String</span></span>

## <span data-ttu-id="40358-133">출력</span><span class="sxs-lookup"><span data-stu-id="40358-133">OUTPUTS</span></span>

### <span data-ttu-id="40358-134">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="40358-134">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="40358-135">상속자</span><span class="sxs-lookup"><span data-stu-id="40358-135">NOTES</span></span>

## <span data-ttu-id="40358-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40358-136">RELATED LINKS</span></span>

[<span data-ttu-id="40358-137">Get-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="40358-137">Get-AzVMDscExtension</span></span>](./Get-AzVMDscExtension.md)

[<span data-ttu-id="40358-138">Set-AzVMDscExtension</span><span class="sxs-lookup"><span data-stu-id="40358-138">Set-AzVMDscExtension</span></span>](./Set-AzVMDscExtension.md)


