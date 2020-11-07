---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsshpublickey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSshPublicKey.md
ms.openlocfilehash: 432de351ae62650ff4e4e2efae0550fab2fa6091
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701379"
---
# <span data-ttu-id="521ad-101">Add-AzVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="521ad-101">Add-AzVMSshPublicKey</span></span>

## <span data-ttu-id="521ad-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="521ad-102">SYNOPSIS</span></span>
<span data-ttu-id="521ad-103">가상 컴퓨터에 대 한 SSH 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-103">Adds the public keys for SSH for a virtual machine.</span></span>

## <span data-ttu-id="521ad-104">구문과</span><span class="sxs-lookup"><span data-stu-id="521ad-104">SYNTAX</span></span>

```
Add-AzVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="521ad-105">설명은</span><span class="sxs-lookup"><span data-stu-id="521ad-105">DESCRIPTION</span></span>
<span data-ttu-id="521ad-106">**AzVMSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통해 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-106">The **Add-AzVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="521ad-107">예제의</span><span class="sxs-lookup"><span data-stu-id="521ad-107">EXAMPLES</span></span>

### <span data-ttu-id="521ad-108">예제 1: 가상 컴퓨터에 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="521ad-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="521ad-109">첫 번째 명령은 **AzVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzVM** cmdlet.</span></span>
<span data-ttu-id="521ad-110">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>
<span data-ttu-id="521ad-111">두 번째 명령은 Path 매개 변수에서 지정 하는 VirtualMachine07의 위치에 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="521ad-112">변수</span><span class="sxs-lookup"><span data-stu-id="521ad-112">PARAMETERS</span></span>

### <span data-ttu-id="521ad-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="521ad-113">-DefaultProfile</span></span>
<span data-ttu-id="521ad-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="521ad-115">-KeyData</span><span class="sxs-lookup"><span data-stu-id="521ad-115">-KeyData</span></span>
<span data-ttu-id="521ad-116">공개 키의 기본 64 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-116">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="521ad-117">SSH를 사용 하거나이 매개 변수에서 지정 하는 키를 사용 하 여 가상 컴퓨터에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-117">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

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

### <span data-ttu-id="521ad-118">-Path</span><span class="sxs-lookup"><span data-stu-id="521ad-118">-Path</span></span>
<span data-ttu-id="521ad-119">가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-119">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="521ad-120">파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-120">If the file already exists, this cmdlet appends the key to the file.</span></span>

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

### <span data-ttu-id="521ad-121">-VM</span><span class="sxs-lookup"><span data-stu-id="521ad-121">-VM</span></span>
<span data-ttu-id="521ad-122">이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-122">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="521ad-123">가상 컴퓨터 개체를 가져오려면 [AzVM](./Get-AzVM.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-123">To obtain a virtual machine object, use the [Get-AzVM](./Get-AzVM.md) cmdlet.</span></span>
<span data-ttu-id="521ad-124">[새 AzVMConfig](./New-AzVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-124">You can use the [New-AzVMConfig](./New-AzVMConfig.md) cmdlet to create a virtual machine object.</span></span>

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

### <span data-ttu-id="521ad-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="521ad-125">CommonParameters</span></span>
<span data-ttu-id="521ad-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="521ad-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="521ad-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="521ad-128">입력</span><span class="sxs-lookup"><span data-stu-id="521ad-128">INPUTS</span></span>

### <span data-ttu-id="521ad-129">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-129">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

### <span data-ttu-id="521ad-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="521ad-130">System.String</span></span>

## <span data-ttu-id="521ad-131">출력</span><span class="sxs-lookup"><span data-stu-id="521ad-131">OUTPUTS</span></span>

### <span data-ttu-id="521ad-132">PSVirtualMachine를 계산 합니다.</span><span class="sxs-lookup"><span data-stu-id="521ad-132">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine</span></span>

## <span data-ttu-id="521ad-133">상속자</span><span class="sxs-lookup"><span data-stu-id="521ad-133">NOTES</span></span>

## <span data-ttu-id="521ad-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="521ad-134">RELATED LINKS</span></span>

[<span data-ttu-id="521ad-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="521ad-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="521ad-136">새로운 AzVMConfig</span><span class="sxs-lookup"><span data-stu-id="521ad-136">New-AzVMConfig</span></span>](./New-AzVMConfig.md)
