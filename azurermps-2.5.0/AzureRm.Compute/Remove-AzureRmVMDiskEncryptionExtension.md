---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 9DDB3672-4C98-4449-9F29-DD9501ED4D3E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermvmdiskencryptionextension
schema: 2.0.0
ms.openlocfilehash: 6c580b862ed2c8a420e8f203131ff9d18d187443
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881982"
---
# <span data-ttu-id="a6a3a-101">Remove-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a6a3a-101">Remove-AzureRmVMDiskEncryptionExtension</span></span>

## <span data-ttu-id="a6a3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6a3a-102">SYNOPSIS</span></span>
<span data-ttu-id="a6a3a-103">가상 컴퓨터에서 디스크 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-103">Removes the disk encryption extension from a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a6a3a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a6a3a-104">SYNTAX</span></span>

```
Remove-AzureRmVMDiskEncryptionExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a6a3a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a6a3a-105">DESCRIPTION</span></span>
<span data-ttu-id="a6a3a-106">**AzureRmVMDiskEncryptionExtension** cmdlet은 가상 컴퓨터에서 디스크 암호화 확장명을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-106">The **Remove-AzureRmVMDiskEncryptionExtension** cmdlet removes the disk encryption extension from a virtual machine.</span></span>
<span data-ttu-id="a6a3a-107">내선 번호를 지정 하지 않으면이 cmdlet은 Windows 운영 체제 또는 Azurediskencryption Forlinux for Linux 기반 가상 컴퓨터를 실행 하는 가상 컴퓨터에 대 한 기본 이름 AzureDiskEncryption으로 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-107">If no extension name is specified, this cmdlet removes the extension with default name AzureDiskEncryption for virtual machines that run the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machines.</span></span>
<span data-ttu-id="a6a3a-108">이 cmdlet은 가상 컴퓨터에서 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-108">This cmdlet does not disable encryption on the virtual machine.</span></span>
<span data-ttu-id="a6a3a-109">가상 컴퓨터에서 확장과 연결 된 확장 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-109">It removes the extension and the associated extension configuration from the virtual machine.</span></span>

## <span data-ttu-id="a6a3a-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a6a3a-110">EXAMPLES</span></span>

### <span data-ttu-id="a6a3a-111">예제 1: 가상 머신에서 디스크 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-111">Example 1: Remove the disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM"
```

<span data-ttu-id="a6a3a-112">이 명령은 Windows 운영 체제 또는 MyTestVM 라는 Linux 용 Azurediskencryption Forlinux를 실행 하는 가상 컴퓨터에 대 한 기본 이름 AzureDiskEncryption으로 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-112">This command removes the extension with default name AzureDiskEncryption for a virtual machine that runs the Windows operating system or AzureDiskEncryptionForLinux for Linux based virtual machine named MyTestVM.</span></span>

### <span data-ttu-id="a6a3a-113">예제 2: 가상 머신에서 특정 디스크 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-113">Example 2: Remove a specific disk encryption extension from a virtual machine.</span></span>
```
PS C:\> Remove-AzureRmVMDiskEncryptionExtension -ResourceGroupName "MyResourceGroup" -VMName "MyTestVM" -Name "MyDiskEncryptionExtension"
```

<span data-ttu-id="a6a3a-114">이 명령은 MyTestVM 이라는 가상 컴퓨터에서 Mydiska 확장 이라는 암호화 확장을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-114">This command removes the encryption extension named MyDiskEncryptionExtension from the virtual machine named MyTestVM.</span></span>

## <span data-ttu-id="a6a3a-115">변수</span><span class="sxs-lookup"><span data-stu-id="a6a3a-115">PARAMETERS</span></span>

### <span data-ttu-id="a6a3a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6a3a-116">-DefaultProfile</span></span>
<span data-ttu-id="a6a3a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-118">-Force</span><span class="sxs-lookup"><span data-stu-id="a6a3a-118">-Force</span></span>
<span data-ttu-id="a6a3a-119">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-119">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-120">-이름</span><span class="sxs-lookup"><span data-stu-id="a6a3a-120">-Name</span></span>
<span data-ttu-id="a6a3a-121">확장을 나타내는 Azure Resource Manager 리소스의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-121">Specifies the name of the Azure Resource Manager resource that represents the extension.</span></span>
<span data-ttu-id="a6a3a-122">Set-AzureRmVMDiskEncryptionExtension cmdlet은이 이름을 Windows 운영 체제를 실행 하는 가상 컴퓨터 및 Linux 용 Azurediskencryption linux 가상 머신에 대 한 AzureDiskEncryption으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-122">The Set-AzureRmVMDiskEncryptionExtension cmdlet sets this name to AzureDiskEncryption for virtual machines that run the Windows operating system and AzureDiskEncryptionForLinux for Linux virtual machines.</span></span>
<span data-ttu-id="a6a3a-123">**AzureRmVMDiskEncryptionExtension** cmdlet에서 기본 이름을 변경 하거나 리소스 관리자 템플릿에서 다른 리소스 이름을 사용 하는 경우에만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-123">Specify this parameter only if you changed the default name in the **Set-AzureRmVMDiskEncryptionExtension** cmdlet or used a different resource name in a Resource Manager template.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ExtensionName

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6a3a-124">-ResourceGroupName</span></span>
<span data-ttu-id="a6a3a-125">가상 컴퓨터에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-125">Specifies the name of the resource group for the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-126">-VMName</span><span class="sxs-lookup"><span data-stu-id="a6a3a-126">-VMName</span></span>
<span data-ttu-id="a6a3a-127">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-127">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a6a3a-128">-Confirm</span></span>
<span data-ttu-id="a6a3a-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a6a3a-130">-WhatIf</span></span>
<span data-ttu-id="a6a3a-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-131">Shows what would happen if the cmdlet runs.</span></span>

<span data-ttu-id="a6a3a-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a6a3a-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6a3a-133">CommonParameters</span></span>
<span data-ttu-id="a6a3a-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6a3a-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6a3a-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6a3a-136">입력</span><span class="sxs-lookup"><span data-stu-id="a6a3a-136">INPUTS</span></span>

### <span data-ttu-id="a6a3a-137">않아야</span><span class="sxs-lookup"><span data-stu-id="a6a3a-137">None</span></span>
<span data-ttu-id="a6a3a-138">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-138">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a6a3a-139">출력</span><span class="sxs-lookup"><span data-stu-id="a6a3a-139">OUTPUTS</span></span>

### <span data-ttu-id="a6a3a-140">이는 PSAzureOperationResponse를 계산 하는 명령입니다.</span><span class="sxs-lookup"><span data-stu-id="a6a3a-140">Microsoft.Azure.Commands.Compute.Models.PSAzureOperationResponse</span></span>

## <span data-ttu-id="a6a3a-141">상속자</span><span class="sxs-lookup"><span data-stu-id="a6a3a-141">NOTES</span></span>

## <span data-ttu-id="a6a3a-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a6a3a-142">RELATED LINKS</span></span>

[<span data-ttu-id="a6a3a-143">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="a6a3a-143">Get-AzureRmVMDiskEncryptionStatus</span></span>](./Get-AzureRmVMDiskEncryptionStatus.md)

[<span data-ttu-id="a6a3a-144">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="a6a3a-144">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


