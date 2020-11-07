---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 413977ee42b0edc2221cbbdcfd34b6130d40f74e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877086"
---
# <span data-ttu-id="4f403-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="4f403-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="4f403-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f403-102">SYNOPSIS</span></span>
<span data-ttu-id="4f403-103">.Rdp 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="4f403-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f403-104">SYNTAX</span></span>

### <span data-ttu-id="4f403-105">다운로드</span><span class="sxs-lookup"><span data-stu-id="4f403-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4f403-106">플러그인</span><span class="sxs-lookup"><span data-stu-id="4f403-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f403-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4f403-107">DESCRIPTION</span></span>
<span data-ttu-id="4f403-108">**AzRemoteDesktopFile** Cmdlet은 원격 데스크톱 프로토콜 (.rdp) 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="4f403-109">예제의</span><span class="sxs-lookup"><span data-stu-id="4f403-109">EXAMPLES</span></span>

### <span data-ttu-id="4f403-110">예제 1: 원격 데스크톱 파일 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f403-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="4f403-111">이 명령은 VirtualMachine07 이라는 가상 컴퓨터에 대 한 원격 데스크톱 파일을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="4f403-112">명령 결과는 D:\RemoteDesktopFile07.rdp. 라는 파일에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="4f403-113">변수</span><span class="sxs-lookup"><span data-stu-id="4f403-113">PARAMETERS</span></span>

### <span data-ttu-id="4f403-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f403-114">-DefaultProfile</span></span>
<span data-ttu-id="4f403-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4f403-116">-시작</span><span class="sxs-lookup"><span data-stu-id="4f403-116">-Launch</span></span>
<span data-ttu-id="4f403-117">이 cmdlet이 .rdp 파일을 가져온 후 원격 데스크톱을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

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

### <span data-ttu-id="4f403-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="4f403-118">-LocalPath</span></span>
<span data-ttu-id="4f403-119">이 cmdlet이 .rdp 파일을 저장 하는 로컬 전체 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

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

### <span data-ttu-id="4f403-120">-이름</span><span class="sxs-lookup"><span data-stu-id="4f403-120">-Name</span></span>
<span data-ttu-id="4f403-121">이 cmdlet이 가져오는 가용성 집합의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

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

### <span data-ttu-id="4f403-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f403-122">-ResourceGroupName</span></span>
<span data-ttu-id="4f403-123">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="4f403-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f403-124">CommonParameters</span></span>
<span data-ttu-id="4f403-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f403-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4f403-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f403-127">입력</span><span class="sxs-lookup"><span data-stu-id="4f403-127">INPUTS</span></span>

### <span data-ttu-id="4f403-128">않아야</span><span class="sxs-lookup"><span data-stu-id="4f403-128">None</span></span>
<span data-ttu-id="4f403-129">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f403-129">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="4f403-130">출력</span><span class="sxs-lookup"><span data-stu-id="4f403-130">OUTPUTS</span></span>

## <span data-ttu-id="4f403-131">상속자</span><span class="sxs-lookup"><span data-stu-id="4f403-131">NOTES</span></span>

## <span data-ttu-id="4f403-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f403-132">RELATED LINKS</span></span>

