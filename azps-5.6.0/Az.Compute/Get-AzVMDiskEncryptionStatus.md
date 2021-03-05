---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azvmdiskencryptionstatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMDiskEncryptionStatus.md
ms.openlocfilehash: 7d0a7537594bb41fbcc41a7ddf457820c9b29dd1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981008"
---
# <span data-ttu-id="8b671-101">Get-AzVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="8b671-101">Get-AzVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="8b671-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8b671-102">SYNOPSIS</span></span>
<span data-ttu-id="8b671-103">가상 머신의 암호화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-103">Gets the encryption status of the virtual machine.</span></span>

## <span data-ttu-id="8b671-104">구문</span><span class="sxs-lookup"><span data-stu-id="8b671-104">SYNTAX</span></span>

```
Get-AzVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8b671-105">설명</span><span class="sxs-lookup"><span data-stu-id="8b671-105">DESCRIPTION</span></span>
<span data-ttu-id="8b671-106">**Get-AzVMDiskEncryptionStatus** cmdlet은 가상 머신의 암호화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-106">The **Get-AzVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="8b671-107">운영 체제 및 데이터 볼륨의 암호화 상태를 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="8b671-108">암호화 상태 외에도 운영 체제 볼륨에 대한 암호화 키 및 키 암호화 키가 있는 **KeyVaults의** 암호화 비밀 URL, 키 암호화 키 URL, 리소스 아이디도 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="8b671-109">예제</span><span class="sxs-lookup"><span data-stu-id="8b671-109">EXAMPLES</span></span>

### <span data-ttu-id="8b671-110">예제 1: 가상 머신의 암호화 상태 확인</span><span class="sxs-lookup"><span data-stu-id="8b671-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="8b671-111">이 명령은 VM001이라는 가상 머신의 암호화 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="8b671-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8b671-112">PARAMETERS</span></span>

### <span data-ttu-id="8b671-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8b671-113">-DefaultProfile</span></span>
<span data-ttu-id="8b671-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8b671-115">-ExtensionPublisherName</span><span class="sxs-lookup"><span data-stu-id="8b671-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="8b671-116">확장 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-116">The extension publisher name.</span></span> <span data-ttu-id="8b671-117">이 매개 변수를 지정하여 "Microsoft.Azure.Security"의 기본값을 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

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

### <span data-ttu-id="8b671-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="8b671-118">-ExtensionType</span></span>
<span data-ttu-id="8b671-119">확장 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-119">The extension type.</span></span> <span data-ttu-id="8b671-120">이 매개 변수를 지정하여 Windows VM에 대한 "AzureDiskEncryption" 및 Linux VM에 대한 "AzureDiskEncryptionForLinux"의 기본값을 오버라이드합니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

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

### <span data-ttu-id="8b671-121">-Name</span><span class="sxs-lookup"><span data-stu-id="8b671-121">-Name</span></span>
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

### <span data-ttu-id="8b671-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8b671-122">-ResourceGroupName</span></span>
<span data-ttu-id="8b671-123">가상 머신의 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="8b671-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="8b671-124">-VMName</span></span>
<span data-ttu-id="8b671-125">가상 머신의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="8b671-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8b671-126">CommonParameters</span></span>
<span data-ttu-id="8b671-127">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8b671-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8b671-128">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8b671-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8b671-129">입력</span><span class="sxs-lookup"><span data-stu-id="8b671-129">INPUTS</span></span>

### <span data-ttu-id="8b671-130">System.String</span><span class="sxs-lookup"><span data-stu-id="8b671-130">System.String</span></span>

## <span data-ttu-id="8b671-131">출력</span><span class="sxs-lookup"><span data-stu-id="8b671-131">OUTPUTS</span></span>

### <span data-ttu-id="8b671-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span><span class="sxs-lookup"><span data-stu-id="8b671-132">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="8b671-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8b671-133">NOTES</span></span>

## <span data-ttu-id="8b671-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8b671-134">RELATED LINKS</span></span>

[<span data-ttu-id="8b671-135">Remove-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8b671-135">Remove-AzVMDiskEncryptionExtension</span></span>](./Remove-AzVMDiskEncryptionExtension.md)

[<span data-ttu-id="8b671-136">Set-AzVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="8b671-136">Set-AzVMDiskEncryptionExtension</span></span>](./Set-AzVMDiskEncryptionExtension.md)


