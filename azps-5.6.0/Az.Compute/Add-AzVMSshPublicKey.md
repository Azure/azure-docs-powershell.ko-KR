---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 4c6d2b3376bb5e92d048db61d68c7cfb1b94ee01
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981115"
---
# <span data-ttu-id="885d3-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="885d3-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="885d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="885d3-102">SYNOPSIS</span></span>
<span data-ttu-id="885d3-103">VM을 만들 때만 가상 머신의 SSH에 대한 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="885d3-104">구문</span><span class="sxs-lookup"><span data-stu-id="885d3-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="885d3-105">설명</span><span class="sxs-lookup"><span data-stu-id="885d3-105">DESCRIPTION</span></span>
<span data-ttu-id="885d3-106">**Add-AzVMSshPublicKey** cmdlet은 SSH(Secure Shell)를 통해 Linux 가상 머신에 연결하는 데 사용할 수 있는 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="885d3-107">업데이트-AzVM 없이 VM을 생성한 후 이 명령을 사용할 수 없습니다. Update-AzVM에서 명령을 사용하는 경우 명령이 오류가 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="885d3-108">예제</span><span class="sxs-lookup"><span data-stu-id="885d3-108">EXAMPLES</span></span>

### <span data-ttu-id="885d3-109">예제 1: 가상 머신에 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="885d3-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="885d3-110">첫 번째 명령은 **Get-AzVM** cmdlet을 사용하여 VirtualMachine07이라는 가상 머신을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="885d3-111">명령은 가상 머신을 $VirtualMachine 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="885d3-112">두 번째 명령은 Path 매개 변수가 지정하는 VirtualMachine07의 위치에 공개 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="885d3-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="885d3-113">PARAMETERS</span></span>

### <span data-ttu-id="885d3-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="885d3-114">-DefaultProfile</span></span>
<span data-ttu-id="885d3-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="885d3-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="885d3-116">-KeyData</span></span>
<span data-ttu-id="885d3-117">공개 키의 기본 64 인코딩을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="885d3-118">SSH를 사용하거나 이 매개 변수가 지정하는 키를 사용하여 Linux 가상 머신에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="885d3-119">-Path</span><span class="sxs-lookup"><span data-stu-id="885d3-119">-Path</span></span>
<span data-ttu-id="885d3-120">이 cmdlet은 SSH 공개 키를 저장하는 가상 머신에 파일의 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="885d3-121">파일이 이미 있는 경우 이 cmdlet은 파일에 키를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="885d3-122">-VM</span><span class="sxs-lookup"><span data-stu-id="885d3-122">-VM</span></span>
<span data-ttu-id="885d3-123">이 cmdlet이 수정하는 가상 머신 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="885d3-124">가상 머신 개체를 얻은 경우 [Get-AzVM](./Get-AzVM.md) cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="885d3-125">[New-AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용하여 가상 머신 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="885d3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="885d3-126">CommonParameters</span></span>
<span data-ttu-id="885d3-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="885d3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="885d3-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="885d3-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="885d3-129">입력</span><span class="sxs-lookup"><span data-stu-id="885d3-129">INPUTS</span></span>

### <span data-ttu-id="885d3-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="885d3-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="885d3-131">System.String</span><span class="sxs-lookup"><span data-stu-id="885d3-131">System.String</span></span>

## <span data-ttu-id="885d3-132">출력</span><span class="sxs-lookup"><span data-stu-id="885d3-132">OUTPUTS</span></span>

### <span data-ttu-id="885d3-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span><span class="sxs-lookup"><span data-stu-id="885d3-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="885d3-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="885d3-134">NOTES</span></span>

## <span data-ttu-id="885d3-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="885d3-135">RELATED LINKS</span></span>

[<span data-ttu-id="885d3-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="885d3-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="885d3-137">New-AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="885d3-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
