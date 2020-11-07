---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/set-azdiskimagereference
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Set-AzDiskImageReference.md
ms.openlocfilehash: 3a18c56d01481e9e8096725685a9a60aff7dc8f6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697254"
---
# <span data-ttu-id="9ba15-101">Set-AzDiskImageReference</span><span class="sxs-lookup"><span data-stu-id="9ba15-101">Set-AzDiskImageReference</span></span>

## <span data-ttu-id="9ba15-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba15-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba15-103">Disk 개체에 대 한 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-103">Sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="9ba15-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9ba15-104">SYNTAX</span></span>

```
Set-AzDiskImageReference [-Disk] <PSDisk> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9ba15-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9ba15-105">DESCRIPTION</span></span>
<span data-ttu-id="9ba15-106">**Set-AzDiskImageReference** cmdlet은 disk 개체의 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-106">The **Set-AzDiskImageReference** cmdlet sets the image reference properties on a disk object.</span></span>

## <span data-ttu-id="9ba15-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9ba15-107">EXAMPLES</span></span>

### <span data-ttu-id="9ba15-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ba15-108">Example 1</span></span>
```
PS C:\> $diskconfig = New-AzDiskConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskconfig = Set-AzDiskImageReference -Disk $diskconfig -Id $image -Lun 0;
PS C:\> New-AzDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -Disk $diskconfig;
```

<span data-ttu-id="9ba15-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형의 10GB 크기의 로컬 디스크 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-109">The first command creates a local disk object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="9ba15-110">Windows OS 종류도 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="9ba15-111">두 번째 명령은 disk 개체의 이미지 id와 논리 단위 번호 0을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-111">The second command sets the image id and the logical unit number 0 for the disk object.</span></span>
<span data-ttu-id="9ba15-112">마지막 명령은 disk 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '에 이름이 ' Disk01 ' 인 디스크를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-112">The last command takes the disk object and creates a disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="9ba15-113">변수</span><span class="sxs-lookup"><span data-stu-id="9ba15-113">PARAMETERS</span></span>

### <span data-ttu-id="9ba15-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba15-114">-DefaultProfile</span></span>
<span data-ttu-id="9ba15-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9ba15-116">-디스크</span><span class="sxs-lookup"><span data-stu-id="9ba15-116">-Disk</span></span>
<span data-ttu-id="9ba15-117">로컬 디스크 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-117">Specifies a local disk object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba15-118">-Id</span><span class="sxs-lookup"><span data-stu-id="9ba15-118">-Id</span></span>
<span data-ttu-id="9ba15-119">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="9ba15-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="9ba15-120">-Lun</span></span>
<span data-ttu-id="9ba15-121">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ba15-122">-확인</span><span class="sxs-lookup"><span data-stu-id="9ba15-122">-Confirm</span></span>
<span data-ttu-id="9ba15-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9ba15-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9ba15-124">-WhatIf</span></span>
<span data-ttu-id="9ba15-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9ba15-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9ba15-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba15-127">CommonParameters</span></span>
<span data-ttu-id="9ba15-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba15-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba15-129">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9ba15-129">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba15-130">입력</span><span class="sxs-lookup"><span data-stu-id="9ba15-130">INPUTS</span></span>

### <span data-ttu-id="9ba15-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="9ba15-131">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

### <span data-ttu-id="9ba15-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9ba15-132">System.String</span></span>

### <span data-ttu-id="9ba15-133">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="9ba15-133">System.Int32</span></span>

## <span data-ttu-id="9ba15-134">출력</span><span class="sxs-lookup"><span data-stu-id="9ba15-134">OUTPUTS</span></span>

### <span data-ttu-id="9ba15-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span><span class="sxs-lookup"><span data-stu-id="9ba15-135">Microsoft.Azure.Commands.Compute.Automation.Models.PSDisk</span></span>

## <span data-ttu-id="9ba15-136">상속자</span><span class="sxs-lookup"><span data-stu-id="9ba15-136">NOTES</span></span>

## <span data-ttu-id="9ba15-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba15-137">RELATED LINKS</span></span>
