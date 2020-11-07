---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: B2B4E132-4A71-4DB8-A7B9-9ED3FE7EB292
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmbginfoextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMBginfoExtension.md
ms.openlocfilehash: d49fae13c69e194f0b31c702670639ce486dad81
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701237"
---
# <span data-ttu-id="1522b-101">Set-AzVMBginfoExtension</span><span class="sxs-lookup"><span data-stu-id="1522b-101">Set-AzVMBginfoExtension</span></span>

## <span data-ttu-id="1522b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1522b-102">SYNOPSIS</span></span>
<span data-ttu-id="1522b-103">가상 컴퓨터에 BGInfo 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-103">Adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="1522b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1522b-104">SYNTAX</span></span>

```
Set-AzVMBginfoExtension [-ResourceGroupName] <String> [-VMName] <String> [-Name <String>]
 [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1522b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1522b-105">DESCRIPTION</span></span>
<span data-ttu-id="1522b-106">**AzVMBGInfoExtension** Cmdlet은 BGInfo 확장을 가상 컴퓨터에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-106">The **Set-AzVMBGInfoExtension** cmdlet adds the BGInfo extension to a virtual machine.</span></span>

## <span data-ttu-id="1522b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1522b-107">EXAMPLES</span></span>

### <span data-ttu-id="1522b-108">예제 1: 가상 컴퓨터에 대 한 BGInfo 확장 추가</span><span class="sxs-lookup"><span data-stu-id="1522b-108">Example 1: Add the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzVMBgInfoExtension -ResourceGroupName "ContosoRG" -VMName "ContosoVM" -Name "ExtensionName" -TypeHandlerVersion "2.1" -Location "West Europe"
```

<span data-ttu-id="1522b-109">이 명령은 ContosoVM 이라는 가상 컴퓨터에 BGInfo 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-109">This command adds the BGInfo extension to virtual machine named ContosoVM.</span></span>
<span data-ttu-id="1522b-110">명령은 가상 컴퓨터의 리소스 그룹과 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-110">The command specifies the resource group and location of the virtual machine.</span></span>
<span data-ttu-id="1522b-111">명령에서 확장명의 이름과 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-111">The command specifies the name and version of the extension.</span></span>

## <span data-ttu-id="1522b-112">변수</span><span class="sxs-lookup"><span data-stu-id="1522b-112">PARAMETERS</span></span>

### <span data-ttu-id="1522b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1522b-113">-DefaultProfile</span></span>
<span data-ttu-id="1522b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1522b-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="1522b-115">-DisableAutoUpgradeMinorVersion</span></span>
<span data-ttu-id="1522b-116">이 cmdlet이 Azure 게스트 에이전트에서 새 부 버전으로 자동으로 확장을 업데이트 하지 않도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-116">Indicates that this cmdlet prevents the Azure guest agent from automatically updating the extension to a newer minor version.</span></span>
<span data-ttu-id="1522b-117">기본적으로이 cmdlet은 게스트 에이전트가 확장을 업데이트할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-117">By default, this cmdlet enables the guest agent to update the extension.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1522b-118">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="1522b-118">-ForceRerun</span></span>
<span data-ttu-id="1522b-119">공용 또는 보호 된 동일한 설정을 사용 하 여 확장을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-119">Specifies that the extension should be run again with the same public or protected settings.</span></span>
<span data-ttu-id="1522b-120">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-120">The value can be any string different from the current value.</span></span>
<span data-ttu-id="1522b-121">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-121">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1522b-122">-위치</span><span class="sxs-lookup"><span data-stu-id="1522b-122">-Location</span></span>
<span data-ttu-id="1522b-123">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-123">Specifies the location of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1522b-124">-이름</span><span class="sxs-lookup"><span data-stu-id="1522b-124">-Name</span></span>
<span data-ttu-id="1522b-125">이 cmdlet가 가상 컴퓨터에 추가 하는 BGInfo 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-125">Specifies the name of the BGInfo extension that this cmdlet adds to a virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1522b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1522b-126">-ResourceGroupName</span></span>
<span data-ttu-id="1522b-127">이 cmdlet이 확장을 추가 하는 가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-127">Specifies the name of the resource group of the virtual machine to which this cmdlet adds an extension.</span></span>

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

### <span data-ttu-id="1522b-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="1522b-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="1522b-129">이 cmdlet가 가상 컴퓨터에 추가 하는 확장의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-129">Specifies the version of the extension that this cmdlet adds to the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: HandlerVersion, Version

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1522b-130">-VMName</span><span class="sxs-lookup"><span data-stu-id="1522b-130">-VMName</span></span>
<span data-ttu-id="1522b-131">이 cmdlet이 BGInfo 확장을 추가 하는 가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-131">Specifies the name of the virtual machine to which this cmdlet adds the BGInfo extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1522b-132">-확인</span><span class="sxs-lookup"><span data-stu-id="1522b-132">-Confirm</span></span>
<span data-ttu-id="1522b-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1522b-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1522b-134">-WhatIf</span></span>
<span data-ttu-id="1522b-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1522b-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1522b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1522b-137">CommonParameters</span></span>
<span data-ttu-id="1522b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1522b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1522b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1522b-140">입력</span><span class="sxs-lookup"><span data-stu-id="1522b-140">INPUTS</span></span>

### <span data-ttu-id="1522b-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1522b-141">System.String</span></span>

### <span data-ttu-id="1522b-142">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1522b-142">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1522b-143">출력</span><span class="sxs-lookup"><span data-stu-id="1522b-143">OUTPUTS</span></span>

### <span data-ttu-id="1522b-144">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="1522b-144">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="1522b-145">상속자</span><span class="sxs-lookup"><span data-stu-id="1522b-145">NOTES</span></span>

## <span data-ttu-id="1522b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1522b-146">RELATED LINKS</span></span>
