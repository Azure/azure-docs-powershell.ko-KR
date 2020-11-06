---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: D93666EC-C252-4E3B-B311-50B6EEA6D4BF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmVMAccessExtension.md
ms.openlocfilehash: c77fe7985e91386cad746c61f5849072e0366615
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525591"
---
# <span data-ttu-id="fb17e-101">Set-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fb17e-101">Set-AzureRmVMAccessExtension</span></span>

## <span data-ttu-id="fb17e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb17e-102">SYNOPSIS</span></span>
<span data-ttu-id="fb17e-103">가상 컴퓨터에 VMAccess 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-103">Adds the VMAccess extension to a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb17e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb17e-104">SYNTAX</span></span>

```
Set-AzureRmVMAccessExtension [-UserName <String>] [-Password <String>] [-ResourceGroupName] <String>
 [-VMName] <String> [-Name <String>] [-TypeHandlerVersion <String>] [-Location <String>]
 [-DisableAutoUpgradeMinorVersion] [-ForceRerun <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fb17e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb17e-105">DESCRIPTION</span></span>
<span data-ttu-id="fb17e-106">**AzureRmVMAccessExtension** cmdlet은 가상 컴퓨터에 vmaccess (Virtual machine Access) 가상 컴퓨터 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-106">The **Set-AzureRmVMAccessExtension** cmdlet adds the Virtual Machine Access (VMAccess) Virtual Machine Extension to a virtual machine.</span></span>
<span data-ttu-id="fb17e-107">VMAccess에서 가상 컴퓨터 사용자 이름 및 암호를 다시 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-107">VMAccess can reset the virtual machine user name and password.</span></span>

## <span data-ttu-id="fb17e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="fb17e-108">EXAMPLES</span></span>

### <span data-ttu-id="fb17e-109">예제 1: VMAccess 확장 추가</span><span class="sxs-lookup"><span data-stu-id="fb17e-109">Example 1: Add a VMAccess extension</span></span>
```
PS C:\> Set-AzureRmVMAccessExtension -ResourceGroupName "ResrouceGroup11" -Location "Central US" -VMName "VirtualMachine07" -Name "ContosoTest" -TypeHandlerVersion "2.0" -UserName "PFuller" -Password "Password"
```

<span data-ttu-id="fb17e-110">이 명령은 ResrouceGroup11의 VirtualMachine07 이라는 가상 컴퓨터에 대 한 VMAccess 확장을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-110">This command adds a VMAccess extension for the virtual machine named VirtualMachine07 in ResrouceGroup11.</span></span>
<span data-ttu-id="fb17e-111">명령은 VMAccess의 이름 및 형식 처리기 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-111">The command specifies the name and type handler version for VMAccess.</span></span>

## <span data-ttu-id="fb17e-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb17e-112">PARAMETERS</span></span>

### <span data-ttu-id="fb17e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb17e-113">-DefaultProfile</span></span>
<span data-ttu-id="fb17e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fb17e-115">-DisableAutoUpgradeMinorVersion</span><span class="sxs-lookup"><span data-stu-id="fb17e-115">-DisableAutoUpgradeMinorVersion</span></span>
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

### <span data-ttu-id="fb17e-116">-ForceRerun</span><span class="sxs-lookup"><span data-stu-id="fb17e-116">-ForceRerun</span></span>
<span data-ttu-id="fb17e-117">이 cmdlet이 확장을 제거 하 고 다시 설치 하지 않고 가상 컴퓨터에서 동일한 확장 구성을 다시 실행 하도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-117">Indicates that this cmdlet forces a rerun of the same extension configuration on the virtual machine without uninstalling and reinstalling the extension.</span></span>
<span data-ttu-id="fb17e-118">값은 현재 값과 다른 문자열 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-118">The value can be any string different from the current value.</span></span>

<span data-ttu-id="fb17e-119">ForceUpdateTag가 변경 되지 않는 경우 공용 또는 보호 된 설정에 대 한 업데이트는 처리기에 의해 계속 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-119">If forceUpdateTag is not changed, updates to public or protected settings are still applied by the handler.</span></span>

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

### <span data-ttu-id="fb17e-120">-위치</span><span class="sxs-lookup"><span data-stu-id="fb17e-120">-Location</span></span>
<span data-ttu-id="fb17e-121">가상 컴퓨터의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-121">Specifies the location of the virtual machine.</span></span>

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

### <span data-ttu-id="fb17e-122">-이름</span><span class="sxs-lookup"><span data-stu-id="fb17e-122">-Name</span></span>
<span data-ttu-id="fb17e-123">이 cmdlet이 추가 하는 확장의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-123">Specifies the name of the extension that this cmdlet adds.</span></span>

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

### <span data-ttu-id="fb17e-124">-암호</span><span class="sxs-lookup"><span data-stu-id="fb17e-124">-Password</span></span>
<span data-ttu-id="fb17e-125">가상 컴퓨터의 새 암호를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-125">Specifies the new password of the virtual machine.</span></span>

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

### <span data-ttu-id="fb17e-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb17e-126">-ResourceGroupName</span></span>
<span data-ttu-id="fb17e-127">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-127">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fb17e-128">-TypeHandlerVersion</span><span class="sxs-lookup"><span data-stu-id="fb17e-128">-TypeHandlerVersion</span></span>
<span data-ttu-id="fb17e-129">이 가상 컴퓨터에 사용할 확장 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-129">Specifies the version of the extension to use for this virtual machine.</span></span>
<span data-ttu-id="fb17e-130">버전을 얻으려면 VMAccessAgent 값을 사용 하 여 cmdlet을 Get-AzureRmVMExtensionImage 실행 합니다. *형식* 매개 변수에 대 한 # e m *m 매개 변수* 및이에 대 한 계산.</span><span class="sxs-lookup"><span data-stu-id="fb17e-130">To obtain the version, run the Get-AzureRmVMExtensionImage cmdlet with a value of Microsoft.Compute for the *PublisherName* parameter and VMAccessAgent for the *Type* parameter.</span></span>

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

### <span data-ttu-id="fb17e-131">-사용자 이름</span><span class="sxs-lookup"><span data-stu-id="fb17e-131">-UserName</span></span>
<span data-ttu-id="fb17e-132">가상 컴퓨터에 대 한 새 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-132">Specifies the new user name for the virtual machine.</span></span>

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

### <span data-ttu-id="fb17e-133">-VMName</span><span class="sxs-lookup"><span data-stu-id="fb17e-133">-VMName</span></span>
<span data-ttu-id="fb17e-134">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-134">Specifies the name of a virtual machine.</span></span>
<span data-ttu-id="fb17e-135">이 cmdlet은이 매개 변수에서 지정 하는 가상 컴퓨터에 대 한 VMAccess를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-135">This cmdlet adds VMAccess for the virtual machine that this parameter specifies.</span></span>

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

### <span data-ttu-id="fb17e-136">-확인</span><span class="sxs-lookup"><span data-stu-id="fb17e-136">-Confirm</span></span>
<span data-ttu-id="fb17e-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fb17e-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb17e-138">-WhatIf</span></span>
<span data-ttu-id="fb17e-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-139">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="fb17e-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fb17e-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb17e-141">CommonParameters</span></span>
<span data-ttu-id="fb17e-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb17e-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb17e-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb17e-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb17e-144">입력</span><span class="sxs-lookup"><span data-stu-id="fb17e-144">INPUTS</span></span>

## <span data-ttu-id="fb17e-145">출력</span><span class="sxs-lookup"><span data-stu-id="fb17e-145">OUTPUTS</span></span>

## <span data-ttu-id="fb17e-146">상속자</span><span class="sxs-lookup"><span data-stu-id="fb17e-146">NOTES</span></span>

## <span data-ttu-id="fb17e-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb17e-147">RELATED LINKS</span></span>

[<span data-ttu-id="fb17e-148">Get-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fb17e-148">Get-AzureRmVMAccessExtension</span></span>](./Get-AzureRmVMAccessExtension.md)

[<span data-ttu-id="fb17e-149">제거-AzureRmVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="fb17e-149">Remove-AzureRmVMAccessExtension</span></span>](./Remove-AzureRmVMAccessExtension.md)

[<span data-ttu-id="fb17e-150">Set-AzureRmVMExtension</span><span class="sxs-lookup"><span data-stu-id="fb17e-150">Set-AzureRmVMExtension</span></span>](./Set-AzureRmVMExtension.md)

[<span data-ttu-id="fb17e-151">Get-AzureRmVMExtensionImage</span><span class="sxs-lookup"><span data-stu-id="fb17e-151">Get-AzureRmVMExtensionImage</span></span>](./Get-AzureRmVMExtensionImage.md)


