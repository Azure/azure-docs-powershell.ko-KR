---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azvmaccessextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzVMAccessExtension.md
ms.openlocfilehash: b0b91e2892f087da6eb510d087980e6f31dd67ef
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701238"
---
# <span data-ttu-id="6d95f-101">Set-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6d95f-101">Set-AzVMAccessExtension</span></span>

## <span data-ttu-id="6d95f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d95f-102">SYNOPSIS</span></span>
<span data-ttu-id="6d95f-103">가상 컴퓨터에 VMAccess 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-103">Adds the VMAccess extension to a virtual machine.</span></span>

## <span data-ttu-id="6d95f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d95f-104">SYNTAX</span></span>

```
Set-AzVMAccessExtension [-Credential <PSCredential>] [-ResourceGroupName] <String> [-VMName] <String>
 [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>] [-DisableAutoUpgradeMinorVersion]
 [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d95f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6d95f-105">DESCRIPTION</span></span>
<span data-ttu-id="6d95f-106">**AzVMAccessExtension** cmdlet은 가상 컴퓨터에 vmaccess (가상 컴퓨터 액세스) 가상 컴퓨터 Vmaccess 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-106">The **Set-AzVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="6d95f-107">VMAccess 확장 프로그램은 임시 암호를 설정 하는 데 사용할 수 있으며, 컴퓨터에 로그인 한 후 즉시 변경 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-107">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span> <span data-ttu-id="6d95f-108">이는 Windows 도메인 컨트롤러에서 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-108">This is not supported on Windows Domain Controllers.</span></span>

## <span data-ttu-id="6d95f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6d95f-109">EXAMPLES</span></span>

### <span data-ttu-id="6d95f-110">예제 1: VMAccess 확장 추가</span><span class="sxs-lookup"><span data-stu-id="6d95f-110">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="6d95f-111">이 명령은 ResrouceGroup11의 VirtualMachine07 이라는 가상 컴퓨터에 대 한 VMAccess 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-111">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="6d95f-112">명령은 VMAccess의 이름 및 형식 처리기 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-112">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="6d95f-113">변수</span><span class="sxs-lookup"><span data-stu-id="6d95f-113">PARAMETERS</span></span>

### <span data-ttu-id="6d95f-114">-Credential</span><span class="sxs-lookup"><span data-stu-id="6d95f-114">-Credential</span></span>
<span data-ttu-id="6d95f-115">가상 컴퓨터에 대 한 사용자 이름 및 암호를 **PSCredential** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-115">Specifies the user name and password for the virtual machine as a **PSCredential** object.</span></span>
<span data-ttu-id="6d95f-116">VM에서 현재 로컬 관리자 계정과 다른 이름을 입력 하면 VMAccess 확장 프로그램이 해당 이름으로 로컬 관리자 계정을 추가 하 고 지정 된 암호를 해당 계정에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-116">If you type a different name than the current local administrator account on your VM, the VMAccess extension will add a local administrator account with that name, and assign your specified password to that account.</span></span> <span data-ttu-id="6d95f-117">VM의 로컬 관리자 계정이 있는 경우 암호를 다시 설정 하 고 계정이 사용 되지 않도록 설정 된 경우 VMAccess 확장에서 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-117">If the local administrator account on your VM exists, it will reset the password and if the account is disabled, the VMAccess extension enables it.</span></span>
<span data-ttu-id="6d95f-118">자격 증명을 얻으려면 Get-Credential cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-118">To obtain a credential, use the Get-Credential cmdlet.</span></span>
<span data-ttu-id="6d95f-119">자세한 내용은을 입력 `Get-Help Get-Credential` 하세요.</span><span class="sxs-lookup"><span data-stu-id="6d95f-119">For more information, type `Get-Help Get-Credential`.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d95f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d95f-120">-DefaultProfile</span></span>
<span data-ttu-id="6d95f-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d95f-122">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="6d95f-122">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="6d95f-123">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="6d95f-123">-ForceRerun</span></span>
<span data-ttu-id="6d95f-124">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-124">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="6d95f-125">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-125">The value can be any string different from the current value.</span></span>
<span data-ttu-id="6d95f-126">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-126">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="6d95f-127">-위치</span><span class="sxs-lookup"><span data-stu-id="6d95f-127">-Location</span></span>
<span data-ttu-id="6d95f-128">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-128">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="6d95f-129">-이름</span><span class="sxs-lookup"><span data-stu-id="6d95f-129">-Name</span></span>
<span data-ttu-id="6d95f-130">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-130">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="6d95f-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6d95f-131">-ResourceGroupName</span></span>
<span data-ttu-id="6d95f-132">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-132">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6d95f-133">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="6d95f-133">-TypeHandlerVersion</span></span>
<span data-ttu-id="6d95f-134">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-134">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="6d95f-135">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="6d95f-135">To obtain the version, run the Get-AzVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span> <span data-ttu-id="6d95f-136">버전 1이 더 이상 사용 되지 않으므로 typeHandlerVersion은 2.0 이상 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-136">The typeHandlerVersion must be 2.0 or greater, as version 1 is deprecated.</span></span>

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

### <span data-ttu-id="6d95f-137">-VMName</span><span class="sxs-lookup"><span data-stu-id="6d95f-137">-VMName</span></span>
<span data-ttu-id="6d95f-138">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-138">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="6d95f-139">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-139">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="6d95f-140">-확인</span><span class="sxs-lookup"><span data-stu-id="6d95f-140">-Confirm</span></span>
<span data-ttu-id="6d95f-141">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-141">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6d95f-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d95f-142">-WhatIf</span></span>
<span data-ttu-id="6d95f-143">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-143">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d95f-144">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-144">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6d95f-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d95f-145">CommonParameters</span></span>
<span data-ttu-id="6d95f-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d95f-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d95f-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d95f-148">입력</span><span class="sxs-lookup"><span data-stu-id="6d95f-148">INPUTS</span></span>

### <span data-ttu-id="6d95f-149">System.webserver. PSCredential</span><span class="sxs-lookup"><span data-stu-id="6d95f-149">System.Management.Automation.PSCredential</span></span>

### <span data-ttu-id="6d95f-150">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6d95f-150">System.String</span></span>

### <span data-ttu-id="6d95f-151">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6d95f-151">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6d95f-152">출력</span><span class="sxs-lookup"><span data-stu-id="6d95f-152">OUTPUTS</span></span>

### <span data-ttu-id="6d95f-153">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="6d95f-153">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="6d95f-154">상속자</span><span class="sxs-lookup"><span data-stu-id="6d95f-154">NOTES</span></span>

## <span data-ttu-id="6d95f-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d95f-155">RELATED LINKS</span></span>

[<span data-ttu-id="6d95f-156">Get-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6d95f-156">Get-AzVMAccessExtension</span></span>](./Get-AzVMAccessExtension.md)

[<span data-ttu-id="6d95f-157">제거-AzVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="6d95f-157">Remove-AzVMAccessExtension</span></span>](./Remove-AzVMAccessExtension.md)

[<span data-ttu-id="6d95f-158">Set-AzVMExtension</span><span class="sxs-lookup"><span data-stu-id="6d95f-158">Set-AzVMExtension</span></span>](./Set-AzVMExtension.md)

[<span data-ttu-id="6d95f-159">Get-AzVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="6d95f-159">Get-AzVMExtensionImage</span></span>](./Get-AzVMExtensionImage.md)


