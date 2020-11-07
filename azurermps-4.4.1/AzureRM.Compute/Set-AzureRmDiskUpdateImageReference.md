---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Set-AzureRmDiskUpdateImageReference.md
ms.openlocfilehash: 777216f6969e661721785601a21ee9604d5eec94
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711613"
---
# <span data-ttu-id="f5b4b-101">Set-AzureRmDiskUpdateImageReference</span><span class="sxs-lookup"><span data-stu-id="f5b4b-101">Set-AzureRmDiskUpdateImageReference</span></span>

## <span data-ttu-id="f5b4b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5b4b-102">SYNOPSIS</span></span>
<span data-ttu-id="f5b4b-103">디스크 업데이트 개체에 대 한 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-103">Sets the image reference properties on a disk update object.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f5b4b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5b4b-104">SYNTAX</span></span>

```
Set-AzureRmDiskUpdateImageReference [-DiskUpdate] <PSDiskUpdate> [[-Id] <String>] [[-Lun] <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f5b4b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5b4b-105">DESCRIPTION</span></span>
<span data-ttu-id="f5b4b-106">**Set-AzureRmDiskUpdateImageReference** cmdlet은 디스크 업데이트 개체의 이미지 참조 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-106">The **Set-AzureRmDiskUpdateImageReference** cmdlet sets the image reference properties on a disk update object.</span></span>

## <span data-ttu-id="f5b4b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5b4b-107">EXAMPLES</span></span>

### <span data-ttu-id="f5b4b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5b4b-108">Example 1</span></span>
```
PS C:\> $diskupdateconfig = New-AzureRmDiskUpdateConfig -DiskSizeGB 10 -AccountType PremiumLRS -OsType Windows -CreateOption FromImage;
PS C:\> $image = '/subscriptions/0000000-0000-0000-0000-000000000000/resourceGroups/ResourceGroup01/providers/Microsoft.Compute/images/TestImage123';        
PS C:\> $diskupdateconfig = Set-AzureRmDiskUpdateImageReference -Disk $diskupdateconfig -Id $image -Lun 0;
PS C:\> Update-AzureRmDisk -ResourceGroupName 'ResourceGroup01' -DiskName 'Disk01' -DiskUpdate $diskupdateconfig;
```

<span data-ttu-id="f5b4b-109">첫 번째 명령은 Premium_LRS 저장소 계정 유형에 서 크기가 10GB 인 로컬 디스크 업데이트 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-109">The first command creates a local disk update object with size 10GB in Premium_LRS storage account type.</span></span>  <span data-ttu-id="f5b4b-110">Windows OS 종류도 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-110">It also sets Windows OS type.</span></span>
<span data-ttu-id="f5b4b-111">두 번째 명령은 디스크 업데이트 개체의 이미지 id와 논리 단위 번호 0을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-111">The second command sets the image id and the logical unit number 0 for the disk update object.</span></span>
<span data-ttu-id="f5b4b-112">마지막 명령은 disk update 개체를 사용 하 여 리소스 그룹 ' ResourceGroup01 '의 이름이 ' Disk01 ' 인 기존 디스크를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-112">The last command takes the disk update object and updates an existing disk with name 'Disk01' in resource group 'ResourceGroup01'.</span></span>

## <span data-ttu-id="f5b4b-113">변수</span><span class="sxs-lookup"><span data-stu-id="f5b4b-113">PARAMETERS</span></span>

### <span data-ttu-id="f5b4b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5b4b-114">-DefaultProfile</span></span>
<span data-ttu-id="f5b4b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f5b4b-116">-DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f5b4b-116">-DiskUpdate</span></span>
<span data-ttu-id="f5b4b-117">로컬 디스크 업데이트 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-117">Specifies a local disk update object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSDiskUpdate
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f5b4b-118">-Id</span><span class="sxs-lookup"><span data-stu-id="f5b4b-118">-Id</span></span>
<span data-ttu-id="f5b4b-119">ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-119">Specifies the ID.</span></span>

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

### <span data-ttu-id="f5b4b-120">-Lun</span><span class="sxs-lookup"><span data-stu-id="f5b4b-120">-Lun</span></span>
<span data-ttu-id="f5b4b-121">LUN (논리 단위 번호)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-121">Specifies the logical unit number (LUN).</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f5b4b-122">-확인</span><span class="sxs-lookup"><span data-stu-id="f5b4b-122">-Confirm</span></span>
<span data-ttu-id="f5b4b-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f5b4b-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f5b4b-124">-WhatIf</span></span>
<span data-ttu-id="f5b4b-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-125">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f5b4b-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f5b4b-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5b4b-127">CommonParameters</span></span>
<span data-ttu-id="f5b4b-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5b4b-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5b4b-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5b4b-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5b4b-130">입력</span><span class="sxs-lookup"><span data-stu-id="f5b4b-130">INPUTS</span></span>

### <span data-ttu-id="f5b4b-131">Microsoft. 관리. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f5b4b-131">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>
<span data-ttu-id="f5b4b-132">System.webserver 시스템. Null 허용 ' 1 [[System. Int32, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f5b4b-132">System.String System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f5b4b-133">출력</span><span class="sxs-lookup"><span data-stu-id="f5b4b-133">OUTPUTS</span></span>

### <span data-ttu-id="f5b4b-134">Microsoft. 관리. DiskUpdate</span><span class="sxs-lookup"><span data-stu-id="f5b4b-134">Microsoft.Azure.Management.Compute.Models.DiskUpdate</span></span>

## <span data-ttu-id="f5b4b-135">상속자</span><span class="sxs-lookup"><span data-stu-id="f5b4b-135">NOTES</span></span>

## <span data-ttu-id="f5b4b-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5b4b-136">RELATED LINKS</span></span>

