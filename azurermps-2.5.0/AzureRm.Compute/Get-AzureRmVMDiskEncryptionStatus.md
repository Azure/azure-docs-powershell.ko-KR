---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermvmdiskencryptionstatus
schema: 2.0.0
ms.openlocfilehash: 667ebae58974b2dc68d19daa6a4f3a9d2e98075d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880569"
---
# <span data-ttu-id="d4de6-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="d4de6-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="d4de6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d4de6-102">SYNOPSIS</span></span>
<span data-ttu-id="d4de6-103">가상 컴퓨터의 암호화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d4de6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d4de6-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-ExtensionType <String>] [-ExtensionPublisherName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d4de6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d4de6-105">DESCRIPTION</span></span>
<span data-ttu-id="d4de6-106">**AzureRmVMDiskEncryptionStatus** cmdlet은 가상 컴퓨터의 암호화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="d4de6-107">운영 체제 및 데이터 볼륨의 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="d4de6-108">암호화 상태 외에도 암호화 비밀 URL, 키 암호화 키 URL, 운영 체제 볼륨에 대 한 암호화 키 및 키 암호화 키가 있는 **Keyvaults** 의 리소스 id가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="d4de6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d4de6-109">EXAMPLES</span></span>

### <span data-ttu-id="d4de6-110">예제 1: 가상 컴퓨터의 암호화 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="d4de6-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="d4de6-111">이 명령은 VM001 이라는 가상 컴퓨터의 암호화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="d4de6-112">변수</span><span class="sxs-lookup"><span data-stu-id="d4de6-112">PARAMETERS</span></span>

### <span data-ttu-id="d4de6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d4de6-113">-DefaultProfile</span></span>
<span data-ttu-id="d4de6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d4de6-115">-Extension# ername</span><span class="sxs-lookup"><span data-stu-id="d4de6-115">-ExtensionPublisherName</span></span>
<span data-ttu-id="d4de6-116">확장명 게시자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-116">The extension publisher name.</span></span> <span data-ttu-id="d4de6-117">"Microsoft. i i."의 기본값을 재정의 하려면이 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-117">Specify this parameter only to override the default value of "Microsoft.Azure.Security".</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4de6-118">-ExtensionType</span><span class="sxs-lookup"><span data-stu-id="d4de6-118">-ExtensionType</span></span>
<span data-ttu-id="d4de6-119">확장 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-119">The extension type.</span></span> <span data-ttu-id="d4de6-120">이 매개 변수를 지정 하면 Windows Vm에 대 한 "AzureDiskEncryption"의 기본값을 재정의 하 고 Linux 용으로 "Azurediskencryption Forlinux"를 재정의할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-120">Specify this parameter to override its default value of "AzureDiskEncryption" for Windows VMs and "AzureDiskEncryptionForLinux" for Linux VMs.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d4de6-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d4de6-121">-Name</span></span>
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

### <span data-ttu-id="d4de6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d4de6-122">-ResourceGroupName</span></span>
<span data-ttu-id="d4de6-123">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-123">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="d4de6-124">-VMName</span><span class="sxs-lookup"><span data-stu-id="d4de6-124">-VMName</span></span>
<span data-ttu-id="d4de6-125">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-125">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="d4de6-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d4de6-126">CommonParameters</span></span>
<span data-ttu-id="d4de6-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d4de6-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d4de6-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d4de6-129">입력</span><span class="sxs-lookup"><span data-stu-id="d4de6-129">INPUTS</span></span>

### <span data-ttu-id="d4de6-130">않아야</span><span class="sxs-lookup"><span data-stu-id="d4de6-130">None</span></span>
<span data-ttu-id="d4de6-131">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d4de6-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="d4de6-132">출력</span><span class="sxs-lookup"><span data-stu-id="d4de6-132">OUTPUTS</span></span>

### <span data-ttu-id="d4de6-133">Azurediskencryption Extensioncontext 확장명 AzureDiskEncryption.</span><span class="sxs-lookup"><span data-stu-id="d4de6-133">Microsoft.Azure.Commands.Compute.Extension.AzureDiskEncryption.AzureDiskEncryptionExtensionContext</span></span>

## <span data-ttu-id="d4de6-134">상속자</span><span class="sxs-lookup"><span data-stu-id="d4de6-134">NOTES</span></span>

## <span data-ttu-id="d4de6-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d4de6-135">RELATED LINKS</span></span>

[<span data-ttu-id="d4de6-136">제거-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d4de6-136">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="d4de6-137">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="d4de6-137">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


