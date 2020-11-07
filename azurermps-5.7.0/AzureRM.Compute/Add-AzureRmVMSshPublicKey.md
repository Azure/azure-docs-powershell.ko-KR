---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 3CE367B1-7685-4046-8E9C-CE680B5AE03F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVMSshPublicKey.md
ms.openlocfilehash: b4cbc3ba7dd90d2810c4833fe1b74c13541fcb7a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702387"
---
# <span data-ttu-id="bf777-101">Add-AzureRmVMSshPublicKey</span><span class="sxs-lookup"><span data-stu-id="bf777-101">Add-AzureRmVMSshPublicKey</span></span>

## <span data-ttu-id="bf777-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bf777-102">SYNOPSIS</span></span>
<span data-ttu-id="bf777-103">가상 컴퓨터에 대 한 SSH 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-103">Adds the public keys for SSH for a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bf777-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bf777-104">SYNTAX</span></span>

```
Add-AzureRmVMSshPublicKey [-VM] <PSVirtualMachine> [[-KeyData] <String>] [[-Path] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="bf777-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bf777-105">DESCRIPTION</span></span>
<span data-ttu-id="bf777-106">**AzureRmVMSshPublicKey** Cmdlet은 보안 셸 (SSH)을 통해 가상 컴퓨터에 연결 하는 데 사용할 수 있는 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-106">The **Add-AzureRmVMSshPublicKey** cmdlet adds the public keys that you can use to connect to a virtual machine over Secure Shell (SSH).</span></span>

## <span data-ttu-id="bf777-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bf777-107">EXAMPLES</span></span>

### <span data-ttu-id="bf777-108">예제 1: 가상 컴퓨터에 공개 키 추가</span><span class="sxs-lookup"><span data-stu-id="bf777-108">Example 1: Add a public key to a virtual machine</span></span>
```
PS C:\> $VirtualMachine = Get-AzureRmVM -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07"
PS C:\> $VirtualMachine = Add-AzureRmVMSshPublicKey -VM $VirtualMachine -KeyData "MIIDszCCApugAwIBAgIJALBV9YJCF/tAMA0GCSq12Ib3DQEB21QUAMEUxCzAJBgNV" -Path "/home/admin/.ssh/authorized_keys"
```

<span data-ttu-id="bf777-109">첫 번째 명령은 **AzureRmVM** cmdlet을 사용 하 여 VirtualMachine07 이라는 가상 컴퓨터를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-109">The first command gets the virtual machine named VirtualMachine07 by using the **Get-AzureRmVM** cmdlet.</span></span>
<span data-ttu-id="bf777-110">명령이 가상 컴퓨터를 $VirtualMachine 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-110">The command stores the virtual machine in the $VirtualMachine variable.</span></span>

<span data-ttu-id="bf777-111">두 번째 명령은 Path 매개 변수에서 지정 하는 VirtualMachine07의 위치에 공개 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-111">The second command adds the public key to the location on VirtualMachine07 that the Path parameter specifies.</span></span>

## <span data-ttu-id="bf777-112">변수</span><span class="sxs-lookup"><span data-stu-id="bf777-112">PARAMETERS</span></span>

### <span data-ttu-id="bf777-113">-KeyData</span><span class="sxs-lookup"><span data-stu-id="bf777-113">-KeyData</span></span>
<span data-ttu-id="bf777-114">공개 키의 기본 64 인코딩을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-114">Specifies a base 64 encoding of a public key.</span></span>
<span data-ttu-id="bf777-115">SSH를 사용 하거나이 매개 변수에서 지정 하는 키를 사용 하 여 가상 컴퓨터에 연결할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-115">You can connect to a virtual machine by using SSH or by using the key that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf777-116">-Path</span><span class="sxs-lookup"><span data-stu-id="bf777-116">-Path</span></span>
<span data-ttu-id="bf777-117">가상 머신에서이 cmdlet이 SSH 공개 키를 저장 하는 파일의 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-117">Specifies the full path of a file, on the virtual machine, where this cmdlet stores the SSH public key.</span></span>
<span data-ttu-id="bf777-118">파일이 이미 있는 경우이 cmdlet은 파일에 키를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-118">If the file already exists, this cmdlet appends the key to the file.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bf777-119">-VM</span><span class="sxs-lookup"><span data-stu-id="bf777-119">-VM</span></span>
<span data-ttu-id="bf777-120">이 cmdlet이 수정 하는 가상 컴퓨터 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-120">Specifies the virtual machine object that this cmdlet modifies.</span></span>
<span data-ttu-id="bf777-121">가상 컴퓨터 개체를 가져오려면 [AzureRmVM](./Get-AzureRmVM.md) cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-121">To obtain a virtual machine object, use the [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet.</span></span>
<span data-ttu-id="bf777-122">[새 AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet을 사용 하 여 가상 컴퓨터 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-122">You can use the [New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet to create a virtual machine object.</span></span>

```yaml
Type: PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bf777-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bf777-123">CommonParameters</span></span>
<span data-ttu-id="bf777-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bf777-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bf777-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bf777-126">입력</span><span class="sxs-lookup"><span data-stu-id="bf777-126">INPUTS</span></span>

### <span data-ttu-id="bf777-127">않아야</span><span class="sxs-lookup"><span data-stu-id="bf777-127">None</span></span>
<span data-ttu-id="bf777-128">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bf777-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bf777-129">출력</span><span class="sxs-lookup"><span data-stu-id="bf777-129">OUTPUTS</span></span>

## <span data-ttu-id="bf777-130">상속자</span><span class="sxs-lookup"><span data-stu-id="bf777-130">NOTES</span></span>

## <span data-ttu-id="bf777-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bf777-131">RELATED LINKS</span></span>

[<span data-ttu-id="bf777-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="bf777-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="bf777-133">새로운 AzureRmVMConfig</span><span class="sxs-lookup"><span data-stu-id="bf777-133">New-AzureRmVMConfig</span></span>](./New-AzureRmVMConfig.md)
