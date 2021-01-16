---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98363763"
---
# <span data-ttu-id="5c832-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5c832-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="5c832-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5c832-102">SYNOPSIS</span></span>
<span data-ttu-id="5c832-103">가상 머신에서 디스크 암호화 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="5c832-104">구문</span><span class="sxs-lookup"><span data-stu-id="5c832-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5c832-105">설명</span><span class="sxs-lookup"><span data-stu-id="5c832-105">DESCRIPTION</span></span>
<span data-ttu-id="5c832-106">**Remove-AzVMDiskEncryptionExtension** cmdlet은 가상 머신에서 디스크 암호화 확장 및 연결된 확장 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="5c832-107">확장 이름이 지정되지 않은 경우 이 cmdlet은 Windows 운영 체제를 실행하고 Linux 기반 가상 머신용 AzureDiskEncryptionForLinux를 실행한 가상 머신에 대한 기본 이름 AzureDiskEncryption을 사용하여 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="5c832-108">가상 머신에서 암호화를 처음 사용하지 않도록 설정하지 않은 경우 이 cmdlet이 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="5c832-109">가상 머신에서 암호화를 사용하지 않도록 설정하기 위해 [Disable-AzVMDiskEncryption을 사용합니다.](./Disable-AzVMDiskEncryption.md)</span><span class="sxs-lookup"><span data-stu-id="5c832-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="5c832-110">예제</span><span class="sxs-lookup"><span data-stu-id="5c832-110">EXAMPLES</span></span>

### <span data-ttu-id="5c832-111">예제 1: 가상 머신에서 디스크 암호화 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="5c832-112">이 명령은 Windows 운영 체제를 실행하고 MyTestVM이라는 Linux 기반 가상 머신용 AzureDiskEncryptionForLinux를 실행하는 가상 머신에 대한 기본 이름의 AzureDiskEncryption을 사용하여 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="5c832-113">예제 2: 가상 머신에서 특정 디스크 암호화 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="5c832-114">이 명령은 MyTestVM이라는 가상 머신에서 MyDiskEncryptionExtension이라는 암호화 확장을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="5c832-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5c832-115">PARAMETERS</span></span>

### <span data-ttu-id="5c832-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5c832-116">-DefaultProfile</span></span>
<span data-ttu-id="5c832-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5c832-118">-Force</span><span class="sxs-lookup"><span data-stu-id="5c832-118">-Force</span></span>
<span data-ttu-id="5c832-119">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="5c832-120">-Name</span><span class="sxs-lookup"><span data-stu-id="5c832-120">-Name</span></span>
<span data-ttu-id="5c832-121">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="5c832-122">이 Set-AzVMDiskEncryptionExtension cmdlet은 Windows 운영 체제를 실행하고 Linux 가상 머신용 AzureDiskEncryptionForLinux를 실행한 가상 머신의 경우 이 이름을 AzureDiskEncryption으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="5c832-123">**Set-AzVMDiskEncryptionExtension** cmdlet에서 기본 이름을 변경하거나 Resource Manager 템플릿에서 다른 리소스 이름을 사용한 경우 이 매개 변수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5c832-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="5c832-124">-NoWait</span></span>
<span data-ttu-id="5c832-125">작업을 시작하고 작업이 완료되기 전에 즉시 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="5c832-126">작업이 성공적으로 완료됐는지 확인하기 위해 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="5c832-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5c832-127">-ResourceGroupName</span></span>
<span data-ttu-id="5c832-128">가상 머신에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="5c832-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="5c832-129">-VMName</span></span>
<span data-ttu-id="5c832-130">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="5c832-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5c832-131">-Confirm</span></span>
<span data-ttu-id="5c832-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5c832-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5c832-133">-WhatIf</span></span>
<span data-ttu-id="5c832-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5c832-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5c832-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5c832-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5c832-136">CommonParameters</span></span>
<span data-ttu-id="5c832-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5c832-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5c832-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="5c832-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5c832-139">입력</span><span class="sxs-lookup"><span data-stu-id="5c832-139">INPUTS</span></span>

### <span data-ttu-id="5c832-140">System.String</span><span class="sxs-lookup"><span data-stu-id="5c832-140">System.String</span></span>

## <span data-ttu-id="5c832-141">출력</span><span class="sxs-lookup"><span data-stu-id="5c832-141">OUTPUTS</span></span>

### <span data-ttu-id="5c832-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="5c832-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="5c832-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5c832-143">NOTES</span></span>

## <span data-ttu-id="5c832-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5c832-144">RELATED LINKS</span></span>

[<span data-ttu-id="5c832-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="5c832-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="5c832-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="5c832-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


