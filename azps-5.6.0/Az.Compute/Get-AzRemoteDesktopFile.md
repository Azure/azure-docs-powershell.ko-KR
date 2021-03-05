---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: d06f8b5efa0a220b20c5324b457a870d5aaa44b2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981056"
---
# <span data-ttu-id="6ec8d-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="6ec8d-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="6ec8d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec8d-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec8d-103">.rdp 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="6ec8d-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ec8d-104">SYNTAX</span></span>

### <span data-ttu-id="6ec8d-105">다운로드</span><span class="sxs-lookup"><span data-stu-id="6ec8d-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6ec8d-106">시작</span><span class="sxs-lookup"><span data-stu-id="6ec8d-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6ec8d-107">설명</span><span class="sxs-lookup"><span data-stu-id="6ec8d-107">DESCRIPTION</span></span>
<span data-ttu-id="6ec8d-108">**Get-AzRemoteDesktopFile** cmdlet은 원격 데스크톱 프로토콜(.rdp) 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="6ec8d-109">예제</span><span class="sxs-lookup"><span data-stu-id="6ec8d-109">EXAMPLES</span></span>

### <span data-ttu-id="6ec8d-110">예제 1: 원격 데스크톱 파일 다운로드</span><span class="sxs-lookup"><span data-stu-id="6ec8d-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="6ec8d-111">이 명령은 VirtualMachine07이라는 가상 머신에 대한 원격 데스크톱 파일을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="6ec8d-112">명령은 D:\RemoteDesktopFile07.rdp라는 파일에 결과를 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="6ec8d-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6ec8d-113">PARAMETERS</span></span>

### <span data-ttu-id="6ec8d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec8d-114">-DefaultProfile</span></span>
<span data-ttu-id="6ec8d-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ec8d-116">-Launch</span><span class="sxs-lookup"><span data-stu-id="6ec8d-116">-Launch</span></span>
<span data-ttu-id="6ec8d-117">.rdp 파일을 얻은 후 이 cmdlet이 원격 데스크톱을 시작하고 나면 이를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec8d-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="6ec8d-118">-LocalPath</span></span>
<span data-ttu-id="6ec8d-119">이 cmdlet이 .rdp 파일을 저장하는 로컬 전체 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec8d-120">-Name</span><span class="sxs-lookup"><span data-stu-id="6ec8d-120">-Name</span></span>
<span data-ttu-id="6ec8d-121">이 cmdlet이 얻을 가용성 집합의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec8d-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec8d-122">-ResourceGroupName</span></span>
<span data-ttu-id="6ec8d-123">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6ec8d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec8d-124">CommonParameters</span></span>
<span data-ttu-id="6ec8d-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec8d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec8d-126">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ec8d-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec8d-127">입력</span><span class="sxs-lookup"><span data-stu-id="6ec8d-127">INPUTS</span></span>

### <span data-ttu-id="6ec8d-128">System.String</span><span class="sxs-lookup"><span data-stu-id="6ec8d-128">System.String</span></span>

## <span data-ttu-id="6ec8d-129">출력</span><span class="sxs-lookup"><span data-stu-id="6ec8d-129">OUTPUTS</span></span>

### <span data-ttu-id="6ec8d-130">System.Void</span><span class="sxs-lookup"><span data-stu-id="6ec8d-130">System.Void</span></span>

## <span data-ttu-id="6ec8d-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ec8d-131">NOTES</span></span>

## <span data-ttu-id="6ec8d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ec8d-132">RELATED LINKS</span></span>
