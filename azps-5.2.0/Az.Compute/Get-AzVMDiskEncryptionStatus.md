---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 4ad5ef08f9c12693a2fa4b4b372ee1320f90fb76
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352905"
---
# <span data-ttu-id="13f2a-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="13f2a-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="13f2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13f2a-102">SYNOPSIS</span></span>
<span data-ttu-id="13f2a-103">가상 머신의 암호화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="13f2a-104">구문</span><span class="sxs-lookup"><span data-stu-id="13f2a-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="13f2a-105">설명</span><span class="sxs-lookup"><span data-stu-id="13f2a-105">DESCRIPTION</span></span>
<span data-ttu-id="13f2a-106">**Get-AzVMDiskEncryptionStatus** cmdlet은 가상 머신의 암호화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="13f2a-107">운영 체제 및 데이터 볼륨의 암호화 상태를 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="13f2a-108">암호화 상태 외에도 운영 체제 볼륨에 대한 암호화 키 및 키 암호화 키가 있는 **KeyVaults의** 암호화 비밀 URL, 키 암호화 키 URL, 리소스 신원도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="13f2a-109">예제</span><span class="sxs-lookup"><span data-stu-id="13f2a-109">EXAMPLES</span></span>

### <span data-ttu-id="13f2a-110">예제 1: 가상 머신의 암호화 상태 확인</span><span class="sxs-lookup"><span data-stu-id="13f2a-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="13f2a-111">이 명령은 VM001이라는 가상 머신의 암호화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="13f2a-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="13f2a-112">PARAMETERS</span></span>

### <span data-ttu-id="13f2a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13f2a-113">-DefaultProfile</span></span>
<span data-ttu-id="13f2a-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="13f2a-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="13f2a-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="13f2a-116">확장 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-116">The extension publisher name.</span></span> <span data-ttu-id="13f2a-117">이 매개 변수를 지정하여 기본값인 "Microsoft.Azure.Security"를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="13f2a-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="13f2a-118">-ExtensionType</span></span>
<span data-ttu-id="13f2a-119">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-119">The extension type.</span></span> <span data-ttu-id="13f2a-120">이 매개 변수를 지정하여 Windows VM의 기본값인 "AzureDiskEncryption"과 Linux VM의 경우 "AzureDiskEncryptionForLinux"를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="13f2a-121">-Name</span><span class="sxs-lookup"><span data-stu-id="13f2a-121">-Name</span></span>
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

### <span data-ttu-id="13f2a-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13f2a-122">-ResourceGroupName</span></span>
<span data-ttu-id="13f2a-123">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="13f2a-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="13f2a-124">-VMName</span></span>
<span data-ttu-id="13f2a-125">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="13f2a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13f2a-126">CommonParameters</span></span>
<span data-ttu-id="13f2a-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13f2a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13f2a-128">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="13f2a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13f2a-129">입력</span><span class="sxs-lookup"><span data-stu-id="13f2a-129">INPUTS</span></span>

### <span data-ttu-id="13f2a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="13f2a-130">System.String</span></span>

## <span data-ttu-id="13f2a-131">출력</span><span class="sxs-lookup"><span data-stu-id="13f2a-131">OUTPUTS</span></span>

### <span data-ttu-id="13f2a-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="13f2a-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="13f2a-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13f2a-133">NOTES</span></span>

## <span data-ttu-id="13f2a-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13f2a-134">RELATED LINKS</span></span>

[<span data-ttu-id="13f2a-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="13f2a-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="13f2a-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="13f2a-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


