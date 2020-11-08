---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: e17b495147c308d20d6d5b950914d26ce56a5706
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212578"
---
# <span data-ttu-id="c1409-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="c1409-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="c1409-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c1409-102">SYNOPSIS</span></span>
<span data-ttu-id="c1409-103">VM만 만들 때 가상 컴퓨터에 대해 SSH 용 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-103">Adds the public keys for SSH for a virtual machine, when only creating the VM.</span></span>

## <span data-ttu-id="c1409-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c1409-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c1409-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c1409-105">DESCRIPTION</span></span>
<span data-ttu-id="c1409-106">**AzVMSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통해 Linux 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a Linux virtual machine over Secure Shell (SSH).</span></span> <span data-ttu-id="c1409-107">VM을 만든 후에 사용할 수 없습니다. 업데이트-AzVM 없이 VM을 만든 후에이를 사용 하려고 하면 오류가 발생 하지 않으며, Update-AzVM 명령을 사용 하는 경우 명령이 오류로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-107">This cannot be used after VM creation, if you try to use this after VM creation without Update-AzVM, there will be no error, if you use the command with Update-AzVM, the command will error.</span></span>

## <span data-ttu-id="c1409-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c1409-108">EXAMPLES</span></span>

### <span data-ttu-id="c1409-109">예제 1: 가상 컴퓨터에 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="c1409-109">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="c1409-110">첫 번째 명령은 **AzVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-110">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="c1409-111">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-111">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="c1409-112">두 번째 명령은 Path 매개 변수에서 지정 하는 VirtualMachine07의 위치에 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-112">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="c1409-113">변수</span><span class="sxs-lookup"><span data-stu-id="c1409-113">PARAMETERS</span></span>

### <span data-ttu-id="c1409-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c1409-114">-DefaultProfile</span></span>
<span data-ttu-id="c1409-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c1409-116">-KeyData</span><span class="sxs-lookup"><span data-stu-id="c1409-116">-KeyData</span></span>
<span data-ttu-id="c1409-117">공개 키의 기본 64 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-117">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="c1409-118">SSH를 사용 하거나이 매개 변수에서 지정 하는 키를 사용 하 여 Linux 가상 컴퓨터에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-118">You can connect to a Linux virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="c1409-119">-Path</span><span class="sxs-lookup"><span data-stu-id="c1409-119">-Path</span></span>
<span data-ttu-id="c1409-120">가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-120">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="c1409-121">파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-121">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="c1409-122">-VM</span><span class="sxs-lookup"><span data-stu-id="c1409-122">-VM</span></span>
<span data-ttu-id="c1409-123">이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-123">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="c1409-124">가상 컴퓨터 개체를 가져오려면 [AzVM](./Get-AzVM.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-124">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="c1409-125">[새 AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-125">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="c1409-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c1409-126">CommonParameters</span></span>
<span data-ttu-id="c1409-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c1409-128">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c1409-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c1409-129">입력</span><span class="sxs-lookup"><span data-stu-id="c1409-129">INPUTS</span></span>

### <span data-ttu-id="c1409-130">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-130">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="c1409-131">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c1409-131">System.String</span></span>

## <span data-ttu-id="c1409-132">출력</span><span class="sxs-lookup"><span data-stu-id="c1409-132">OUTPUTS</span></span>

### <span data-ttu-id="c1409-133">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="c1409-133">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="c1409-134">상속자</span><span class="sxs-lookup"><span data-stu-id="c1409-134">NOTES</span></span>

## <span data-ttu-id="c1409-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c1409-135">RELATED LINKS</span></span>

[<span data-ttu-id="c1409-136">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="c1409-136">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="c1409-137">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="c1409-137">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
