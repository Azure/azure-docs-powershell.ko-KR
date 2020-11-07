---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/get-azurermremotedesktopfile
schema: 2.0.0
ms.openlocfilehash: e8b19272ed7b6c68221e34cef0395f0592b3013d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881157"
---
# <span data-ttu-id="905c6-101">Get-AzureRmRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="905c6-101">Get-AzureRmRemoteDesktopFile</span></span>

## <span data-ttu-id="905c6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="905c6-102">SYNOPSIS</span></span>
<span data-ttu-id="905c6-103">.Rdp 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-103">Gets an .rdp file.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="905c6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="905c6-104">SYNTAX</span></span>

### <span data-ttu-id="905c6-105">다운로드</span><span class="sxs-lookup"><span data-stu-id="905c6-105">Download</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="905c6-106">플러그인</span><span class="sxs-lookup"><span data-stu-id="905c6-106">Launch</span></span>
```
Get-AzureRmRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="905c6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="905c6-107">DESCRIPTION</span></span>
<span data-ttu-id="905c6-108">**AzureRmRemoteDesktopFile** Cmdlet은 원격 데스크톱 프로토콜 (.rdp) 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-108">The **Get-AzureRmRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="905c6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="905c6-109">EXAMPLES</span></span>

### <span data-ttu-id="905c6-110">예제 1: 원격 데스크톱 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="905c6-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzureRmRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="905c6-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대 한 원격 데스크톱 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="905c6-112">명령 결과는 D:\RemoteDesktopFile07.rdp. 라는 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="905c6-113">변수</span><span class="sxs-lookup"><span data-stu-id="905c6-113">PARAMETERS</span></span>

### <span data-ttu-id="905c6-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="905c6-114">-DefaultProfile</span></span>
<span data-ttu-id="905c6-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="905c6-116">-시작</span><span class="sxs-lookup"><span data-stu-id="905c6-116">-Launch</span></span>
<span data-ttu-id="905c6-117">이 cmdlet이 .rdp 파일을 가져온 후 원격 데스크톱을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: Launch
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="905c6-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="905c6-118">-LocalPath</span></span>
<span data-ttu-id="905c6-119">이 cmdlet이 .rdp 파일을 저장 하는 로컬 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: String
Parameter Sets: Download
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: Launch
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="905c6-120">-이름</span><span class="sxs-lookup"><span data-stu-id="905c6-120">-Name</span></span>
<span data-ttu-id="905c6-121">이 cmdlet이 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="905c6-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="905c6-122">-ResourceGroupName</span></span>
<span data-ttu-id="905c6-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="905c6-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="905c6-124">CommonParameters</span></span>
<span data-ttu-id="905c6-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="905c6-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="905c6-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="905c6-127">입력</span><span class="sxs-lookup"><span data-stu-id="905c6-127">INPUTS</span></span>

### <span data-ttu-id="905c6-128">않아야</span><span class="sxs-lookup"><span data-stu-id="905c6-128">None</span></span>
<span data-ttu-id="905c6-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="905c6-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="905c6-130">출력</span><span class="sxs-lookup"><span data-stu-id="905c6-130">OUTPUTS</span></span>

## <span data-ttu-id="905c6-131">상속자</span><span class="sxs-lookup"><span data-stu-id="905c6-131">NOTES</span></span>

## <span data-ttu-id="905c6-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="905c6-132">RELATED LINKS</span></span>

