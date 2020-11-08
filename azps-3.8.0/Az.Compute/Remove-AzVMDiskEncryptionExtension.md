---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azvmdiskencryptionextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzVMDiskEncryptionExtension.md
ms.openlocfilehash: 4c9e66d751b5465f4112b7cb6d971022e43fa023
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043674"
---
# <span data-ttu-id="aff23-101">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="aff23-101">Remove-AzVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="aff23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aff23-102">SYNOPSIS</span></span>
<span data-ttu-id="aff23-103">가상 컴퓨터에서 디스크 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-103">Removes the disk encryption extension from a virtual machine.</span></span>

## <span data-ttu-id="aff23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aff23-104">SYNTAX</span></span>

```
Remove-AzVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>] [-Force]
 [-NoWait] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aff23-105">설명은</span><span class="sxs-lookup"><span data-stu-id="aff23-105">DESCRIPTION</span></span>
<span data-ttu-id="aff23-106">**AzVMDiskEncryptionExtension** cmdlet은 디스크 암호화 확장과 가상 컴퓨터에서 연결 된 확장 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-106">The **Remove-AzVMDiskEncryptionExtension** cmdlet removes the disk encryption extension and the associated extension configuration from a virtual machine.</span></span> <span data-ttu-id="aff23-107">내선 번호를 지정 하지 않으면이 cmdlet은 Windows 운영 체제 또는 Azurediskencryption Forlinux for Linux 기반 가상 컴퓨터를 실행 하는 가상 컴퓨터에 대 한 기본 이름 AzureDiskEncryption으로 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span> 

<span data-ttu-id="aff23-108">가상 컴퓨터의 암호화를 처음으로 사용 하지 않도록 설정 하지 않은 경우이 cmdlet이 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-108">This cmdlet will fail if encryption on the virtual machine has not been first disabled.</span></span>  <span data-ttu-id="aff23-109">가상 머신에서 암호화를 사용 하지 않도록 설정 하려면 [disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md)를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-109">To disable encryption on a virtual machine, use [Disable-AzVMDiskEncryption](./Disable-AzVMDiskEncryption.md).</span></span> 

## <span data-ttu-id="aff23-110">예제의</span><span class="sxs-lookup"><span data-stu-id="aff23-110">EXAMPLES</span></span>

### <span data-ttu-id="aff23-111">예제 1: 가상 머신에서 디스크 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="aff23-112">이 명령은 Windows 운영 체제 또는 MyTestVM 라는 Linux 용 Azurediskencryption Forlinux를 실행 하는 가상 컴퓨터에 대 한 기본 이름 AzureDiskEncryption으로 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="aff23-113">예제 2: 가상 머신에서 특정 디스크 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="aff23-114">이 명령은 MyTestVM 이라는 가상 컴퓨터에서 Mydiska 확장 이라는 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="aff23-115">변수</span><span class="sxs-lookup"><span data-stu-id="aff23-115">PARAMETERS</span></span>

### <span data-ttu-id="aff23-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aff23-116">-DefaultProfile</span></span>
<span data-ttu-id="aff23-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="aff23-118">-Force</span><span class="sxs-lookup"><span data-stu-id="aff23-118">-Force</span></span>
<span data-ttu-id="aff23-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-119">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="aff23-120">-이름</span><span class="sxs-lookup"><span data-stu-id="aff23-120">-Name</span></span>
<span data-ttu-id="aff23-121">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="aff23-122">Set-AzVMDiskEncryptionExtension cmdlet은이 이름을 Windows 운영 체제를 실행 하는 가상 컴퓨터 및 Linux 용 Azurediskencryption linux 가상 머신에 대 한 AzureDiskEncryption으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-122">The Set-AzVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="aff23-123">**AzVMDiskEncryptionExtension** cmdlet에서 기본 이름을 변경 하거나 리소스 관리자 템플릿에서 다른 리소스 이름을 사용 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-123">Specify this parameter only if you changed the default name in the **Set-AzVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

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

### <span data-ttu-id="aff23-124">-NoWait</span><span class="sxs-lookup"><span data-stu-id="aff23-124">-NoWait</span></span>
<span data-ttu-id="aff23-125">작업이 완료 되기 전에 작업을 시작 하 고 즉시 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-125">Starts the operation and returns immediately, before the operation is completed.</span></span> <span data-ttu-id="aff23-126">작업이 성공적으로 완료 되었는지 확인 하려면 다른 메커니즘을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-126">In order to determine if the operation has successfully been completed, use some other mechanism.</span></span>

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

### <span data-ttu-id="aff23-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aff23-127">-ResourceGroupName</span></span>
<span data-ttu-id="aff23-128">가상 컴퓨터에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-128">Specifies the name of the resource group for the virtual machine.</span></span>

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

### <span data-ttu-id="aff23-129">-VMName</span><span class="sxs-lookup"><span data-stu-id="aff23-129">-VMName</span></span>
<span data-ttu-id="aff23-130">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-130">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="aff23-131">-확인</span><span class="sxs-lookup"><span data-stu-id="aff23-131">-Confirm</span></span>
<span data-ttu-id="aff23-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aff23-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aff23-133">-WhatIf</span></span>
<span data-ttu-id="aff23-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aff23-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aff23-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aff23-136">CommonParameters</span></span>
<span data-ttu-id="aff23-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aff23-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aff23-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aff23-139">입력</span><span class="sxs-lookup"><span data-stu-id="aff23-139">INPUTS</span></span>

### <span data-ttu-id="aff23-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="aff23-140">System.String</span></span>

## <span data-ttu-id="aff23-141">출력</span><span class="sxs-lookup"><span data-stu-id="aff23-141">OUTPUTS</span></span>

### <span data-ttu-id="aff23-142">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="aff23-142">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="aff23-143">상속자</span><span class="sxs-lookup"><span data-stu-id="aff23-143">NOTES</span></span>

## <span data-ttu-id="aff23-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aff23-144">RELATED LINKS</span></span>

[<span data-ttu-id="aff23-145">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="aff23-145">Get-AzVMDiskEncryptionStatus</span></span>](./Get-AzVMDiskEncryptionStatus.md)

[<span data-ttu-id="aff23-146">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="aff23-146">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


