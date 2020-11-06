---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: E6F91D2E-6481-44C2-AF21-F62947C3D78C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRmVMDiskEncryptionStatus.md
ms.openlocfilehash: 9ec94d0c11bf9302156355c28566ce16f48ae148
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530559"
---
# <span data-ttu-id="fb245-101">Get-AzureRmVMDiskEncryptionStatus</span><span class="sxs-lookup"><span data-stu-id="fb245-101">Get-AzureRmVMDiskEncryptionStatus</span></span>

## <span data-ttu-id="fb245-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb245-102">SYNOPSIS</span></span>
<span data-ttu-id="fb245-103">가상 컴퓨터의 암호화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-103">Gets the encryption status of the virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb245-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb245-104">SYNTAX</span></span>

```
Get-AzureRmVMDiskEncryptionStatus [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb245-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb245-105">DESCRIPTION</span></span>
<span data-ttu-id="fb245-106">**AzureRmVMDiskEncryptionStatus** cmdlet은 가상 컴퓨터의 암호화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-106">The **Get-AzureRmVMDiskEncryptionStatus** cmdlet gets the encryption status of the virtual machine.</span></span>
<span data-ttu-id="fb245-107">운영 체제 및 데이터 볼륨의 암호화 상태를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-107">It displays the encryption status of the operating system and data volumes.</span></span>
<span data-ttu-id="fb245-108">암호화 상태 외에도 암호화 비밀 URL, 키 암호화 키 URL, 운영 체제 볼륨에 대 한 암호화 키 및 키 암호화 키가 있는 **Keyvaults** 의 리소스 id가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-108">In addition to encryption status, it also displays the encryption secret URL, key encryption key URL, resource IDs of the **KeyVaults** where the encryption key and key encryption key for operating system volume are present.</span></span>

## <span data-ttu-id="fb245-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb245-109">EXAMPLES</span></span>

### <span data-ttu-id="fb245-110">예제 1: 가상 컴퓨터의 암호화 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb245-110">Example 1: Get the encryption status of a virtual machine</span></span>
```
PS C:\> Get-AzureRmVmDiskEncryptionStatus -ResourceGroupName "MyResourceGroup001" -VMName "VM001"
```

<span data-ttu-id="fb245-111">이 명령은 VM001 이라는 가상 컴퓨터의 암호화 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-111">This command gets the encryption status of the virtual machine named VM001.</span></span>

## <span data-ttu-id="fb245-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb245-112">PARAMETERS</span></span>

### <span data-ttu-id="fb245-113">-이름</span><span class="sxs-lookup"><span data-stu-id="fb245-113">-Name</span></span>
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

### <span data-ttu-id="fb245-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb245-114">-ResourceGroupName</span></span>
<span data-ttu-id="fb245-115">가상 컴퓨터의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-115">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="fb245-116">-VMName</span><span class="sxs-lookup"><span data-stu-id="fb245-116">-VMName</span></span>
<span data-ttu-id="fb245-117">가상 컴퓨터의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-117">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="fb245-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb245-118">CommonParameters</span></span>
<span data-ttu-id="fb245-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb245-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb245-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb245-121">입력</span><span class="sxs-lookup"><span data-stu-id="fb245-121">INPUTS</span></span>

### <span data-ttu-id="fb245-122">않아야</span><span class="sxs-lookup"><span data-stu-id="fb245-122">None</span></span>
<span data-ttu-id="fb245-123">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb245-123">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fb245-124">출력</span><span class="sxs-lookup"><span data-stu-id="fb245-124">OUTPUTS</span></span>

## <span data-ttu-id="fb245-125">상속자</span><span class="sxs-lookup"><span data-stu-id="fb245-125">NOTES</span></span>

## <span data-ttu-id="fb245-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb245-126">RELATED LINKS</span></span>

[<span data-ttu-id="fb245-127">제거-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fb245-127">Remove-AzureRmVMDiskEncryptionExtension</span></span>](./Remove-AzureRmVMDiskEncryptionExtension.md)

[<span data-ttu-id="fb245-128">Set-AzureRmVMDiskEncryptionExtension</span><span class="sxs-lookup"><span data-stu-id="fb245-128">Set-AzureRmVMDiskEncryptionExtension</span></span>](./Set-AzureRmVMDiskEncryptionExtension.md)


