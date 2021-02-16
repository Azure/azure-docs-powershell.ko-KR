---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199353"
---
# <span data-ttu-id="d2f6f-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="d2f6f-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="d2f6f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="d2f6f-103">VM을 만들 때만 가상 머신에 대한 SSH에 대한 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="d2f6f-104">구문</span><span class="sxs-lookup"><span data-stu-id="d2f6f-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d2f6f-105">설명</span><span class="sxs-lookup"><span data-stu-id="d2f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="d2f6f-106">**Add-AzVMSshPublicKey** cmdlet은 SSH(Secure Shell)를 통해 Linux 가상 머신에 연결하는 데 사용할 수 있는 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="d2f6f-107">이 명령은 VM을 생성한 후 사용할 수 없습니다. Update-AzVM 없이 VM을 생성한 후에 이 명령을 사용하려고 하면 오류가 없습니다. Update-AzVM과 함께 명령을 사용하는 경우 명령이 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="d2f6f-108">예제</span><span class="sxs-lookup"><span data-stu-id="d2f6f-108">EXAMPLES</span></span>

### <span data-ttu-id="d2f6f-109">예제 1: 가상 머신에 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="d2f6f-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="d2f6f-110">첫 번째 명령은 **Get-AzVM** cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="d2f6f-111">이 명령은 가상 머신을 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="d2f6f-112">두 번째 명령은 Path 매개 변수가 지정하는 VirtualMachine07의 위치에 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="d2f6f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d2f6f-113">PARAMETERS</span></span>

### <span data-ttu-id="d2f6f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2f6f-114">-DefaultProfile</span></span>
<span data-ttu-id="d2f6f-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d2f6f-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="d2f6f-116">-KeyData</span></span>
<span data-ttu-id="d2f6f-117">공개 키의 기본 64 인코딩을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="d2f6f-118">SSH를 사용하거나 이 매개 변수가 지정하는 키를 사용하여 Linux 가상 머신에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f6f-119">-Path</span><span class="sxs-lookup"><span data-stu-id="d2f6f-119">-Path</span></span>
<span data-ttu-id="d2f6f-120">이 cmdlet이 SSH 공개 키를 저장하는 가상 머신에서 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="d2f6f-121">파일이 이미 있는 경우 이 cmdlet은 파일에 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="d2f6f-122">-VM</span><span class="sxs-lookup"><span data-stu-id="d2f6f-122">-VM</span></span>
<span data-ttu-id="d2f6f-123">이 cmdlet이 수정하는 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="d2f6f-124">가상 머신 개체를 얻습니다. [Get-AzVM](./Get-AzVM.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="d2f6f-125">[New-AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d2f6f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2f6f-126">CommonParameters</span></span>
<span data-ttu-id="d2f6f-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2f6f-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="d2f6f-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2f6f-129">입력</span><span class="sxs-lookup"><span data-stu-id="d2f6f-129">INPUTS</span></span>

### <span data-ttu-id="d2f6f-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2f6f-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="d2f6f-131">System.String</span><span class="sxs-lookup"><span data-stu-id="d2f6f-131">System.String</span></span>

## <span data-ttu-id="d2f6f-132">출력</span><span class="sxs-lookup"><span data-stu-id="d2f6f-132">OUTPUTS</span></span>

### <span data-ttu-id="d2f6f-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="d2f6f-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="d2f6f-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d2f6f-134">NOTES</span></span>

## <span data-ttu-id="d2f6f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2f6f-135">RELATED LINKS</span></span>

[<span data-ttu-id="d2f6f-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="d2f6f-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="d2f6f-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="d2f6f-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)