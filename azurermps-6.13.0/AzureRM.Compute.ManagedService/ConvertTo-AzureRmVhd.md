---
external help file: AzureRM.Compute.ManagedService-help.xml
Module Name: AzureRM.Compute.ManagedService
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute.managedservice/convertto-azurermvhd
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute.ManagedService/Commands.Compute.ManagedService/help/ConvertTo-AzureRmVhd.md
ms.openlocfilehash: 0fa0f2d5cb78fe96f05b818b5cbfdabca47cbdee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526259"
---
# <span data-ttu-id="63d96-101">ConvertTo-AzureRmVhd</span><span class="sxs-lookup"><span data-stu-id="63d96-101">ConvertTo-AzureRmVhd</span></span>

## <span data-ttu-id="63d96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63d96-102">SYNOPSIS</span></span>
<span data-ttu-id="63d96-103">Hyper-v VM을 Azure 지원 가상 하드 디스크 파일로 변환</span><span class="sxs-lookup"><span data-stu-id="63d96-103">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="63d96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63d96-104">SYNTAX</span></span>

```
ConvertTo-AzureRmVhd -HyperVVMName <String> -ExportPath <String> [-HyperVServer <String>] [-Force] [-AsJob]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="63d96-105">설명은</span><span class="sxs-lookup"><span data-stu-id="63d96-105">DESCRIPTION</span></span>
<span data-ttu-id="63d96-106">Hyper-v VM을 Azure 지원 가상 하드 디스크 파일로 변환</span><span class="sxs-lookup"><span data-stu-id="63d96-106">Convert Hyper-V VM to Azure supported virtual hard disk files</span></span>

## <span data-ttu-id="63d96-107">예제의</span><span class="sxs-lookup"><span data-stu-id="63d96-107">EXAMPLES</span></span>

### <span data-ttu-id="63d96-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="63d96-108">Example 1</span></span>
```
PS C:\> ConvertTo-AzureRmVhd -HyperVVMName 'test' -ExportPath '.';
.\test\Virtual Hard Disks\Converted\os.vhd
.\test\Virtual Hard Disks\Converted\disk.vhd
```

<span data-ttu-id="63d96-109">' Test ' 라고 하는 Hyper-v VM을 Azure 지원 가상 하드 디스크 파일로 현재 폴더로 변환 합니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-109">Convert Hyper-V VM named 'test' to Azure supported virtual hard disk files to the current folder.</span></span>

## <span data-ttu-id="63d96-110">변수</span><span class="sxs-lookup"><span data-stu-id="63d96-110">PARAMETERS</span></span>

### <span data-ttu-id="63d96-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63d96-111">-AsJob</span></span>
<span data-ttu-id="63d96-112">백그라운드에서 cmdlet을 실행 하 고 작업을 반환 하 여 진행률을 추적 합니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-112">Run cmdlet in the background and return a Job to track progress.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-113">-ExportPath</span><span class="sxs-lookup"><span data-stu-id="63d96-113">-ExportPath</span></span>
<span data-ttu-id="63d96-114">디스크 파일을 포함 하는 내보내기 폴더 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-114">The export folder path that will contain the disk files.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-115">-Force</span><span class="sxs-lookup"><span data-stu-id="63d96-115">-Force</span></span>
<span data-ttu-id="63d96-116">기존 폴더를 찾은 경우에도 내보내기를 강제 합니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-116">Force the export even if existing folder is found.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-117">-HyperVServer</span><span class="sxs-lookup"><span data-stu-id="63d96-117">-HyperVServer</span></span>
<span data-ttu-id="63d96-118">' Localhost '를 기본값으로 사용 하는 Hyper-v 서버 DNS 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-118">The Hyper-V server DNS name, with 'localhost' as the default value.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: Localhost
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-119">-HyperVVMName</span><span class="sxs-lookup"><span data-stu-id="63d96-119">-HyperVVMName</span></span>
<span data-ttu-id="63d96-120">Hyper-v 이름 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-120">The Hyper-V name name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-121">-확인</span><span class="sxs-lookup"><span data-stu-id="63d96-121">-Confirm</span></span>
<span data-ttu-id="63d96-122">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="63d96-123">-WhatIf</span></span>
<span data-ttu-id="63d96-124">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="63d96-125">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63d96-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63d96-126">CommonParameters</span></span>
<span data-ttu-id="63d96-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63d96-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63d96-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63d96-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63d96-129">입력</span><span class="sxs-lookup"><span data-stu-id="63d96-129">INPUTS</span></span>

### <span data-ttu-id="63d96-130">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63d96-130">System.String</span></span>

## <span data-ttu-id="63d96-131">출력</span><span class="sxs-lookup"><span data-stu-id="63d96-131">OUTPUTS</span></span>

### <span data-ttu-id="63d96-132">System.webserver. PathInfo</span><span class="sxs-lookup"><span data-stu-id="63d96-132">System.Management.Automation.PathInfo</span></span>

## <span data-ttu-id="63d96-133">상속자</span><span class="sxs-lookup"><span data-stu-id="63d96-133">NOTES</span></span>

## <span data-ttu-id="63d96-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63d96-134">RELATED LINKS</span></span>
