---
external help file: ''
Module Name: ''
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: c440fa43a4e15abb5ab9f87d5b814fe3cbc55d63
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529031"
---
# <span data-ttu-id="169d3-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="169d3-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="169d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="169d3-102">SYNOPSIS</span></span>
<span data-ttu-id="169d3-103">Hyper-v VM을 Azure 지원 가상 하드 디스크 파일로 변환</span><span class="sxs-lookup"><span data-stu-id="169d3-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="169d3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="169d3-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [<CommonParameters>]
```

## <span data-ttu-id="169d3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="169d3-105">DESCRIPTION</span></span>
<span data-ttu-id="169d3-106">Hyper-v VM을 Azure 지원 가상 하드 디스크 파일로 변환</span><span class="sxs-lookup"><span data-stu-id="169d3-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="169d3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="169d3-107">EXAMPLES</span></span>

### <span data-ttu-id="169d3-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="169d3-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="169d3-109">' Test ' 라고 하는 Hyper-v VM을 Azure 지원 가상 하드 디스크 파일로 현재 폴더로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="169d3-110">변수</span><span class="sxs-lookup"><span data-stu-id="169d3-110">PARAMETERS</span></span>

### <span data-ttu-id="169d3-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="169d3-111">-AsJob</span></span>
<span data-ttu-id="169d3-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="169d3-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="169d3-113">-ExportPath</span></span>
<span data-ttu-id="169d3-114">디스크 파일을 포함 하는 내보내기 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169d3-115">-Force</span><span class="sxs-lookup"><span data-stu-id="169d3-115">-Force</span></span>
<span data-ttu-id="169d3-116">기존 폴더를 찾은 경우에도 내보내기를 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169d3-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="169d3-117">-HyperVServer</span></span>
<span data-ttu-id="169d3-118">' Localhost '를 기본값으로 사용 하는 Hyper-v 서버 DNS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169d3-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="169d3-119">-HyperVVMName</span></span>
<span data-ttu-id="169d3-120">Hyper-v 이름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-120">The Hyper-V name name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="169d3-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="169d3-121">CommonParameters</span></span>
<span data-ttu-id="169d3-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="169d3-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="169d3-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="169d3-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="169d3-124">입력</span><span class="sxs-lookup"><span data-stu-id="169d3-124">INPUTS</span></span>

### <span data-ttu-id="169d3-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="169d3-125">System.String</span></span>

## <span data-ttu-id="169d3-126">출력</span><span class="sxs-lookup"><span data-stu-id="169d3-126">OUTPUTS</span></span>

### <span data-ttu-id="169d3-127">System.webserver. PathInfo</span><span class="sxs-lookup"><span data-stu-id="169d3-127">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="169d3-128">상속자</span><span class="sxs-lookup"><span data-stu-id="169d3-128">NOTES</span></span>

## <span data-ttu-id="169d3-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="169d3-129">RELATED LINKS</span></span>

